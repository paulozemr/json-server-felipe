<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_jogador: "",
      jogadores: [
        {
          id: "2fc1ea4e-8220-482b-8e49-e3f6b1dfc954",
          name: "Jogador 1",
          timeid: "759b5c49-db71-4d82-b199-7a5abd2c4f5b",
        },
        {
          id: "9b46cba2-f989-4e77-aab6-15b6128e21d6",
          name: "Jogador 2",
          timeid: "209c1c2b-6d24-410b-9fca-f03379dcf437",
        },
        {
          id: "2d0025b0-056b-41af-a35c-909aed0cea33",
          name: "Jogador 3",
          timeid: "52f38a69-0bf0-45b4-bfad-5a6a96676632",
        },
        {
          id: "ce5d8c2a-eb49-49e3-ad47-3ffa85ca19be",
          name: "Jogador 4",
          timeid: "1d7ad795-1952-4a2a-a350-6a8293b1ad7c",
        },
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id = uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogador,
        timeid: this.id_time,
      });
    },
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de jogadores</h2>
    </div>
  </div>
  <div class="form-input">
    <input type="text" placeholder="Nome" v-model="novo_jogador" />
    <input type="text" placeholder="ID Time" v-model="id_time" />
    <button @click="salvar">Salvar</button>
  </div>
  <div class="list-items">
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Nome</th>
          <th>Time ID</th>
          <th>Funções</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="jogador in jogadores" :key="jogador.id">
          <td>{{ jogador.id }}</td>
          <td>{{ jogador.name }}</td>
          <td>{{ jogador.timeid }}</td>
          <td><select>
              <option disabled>...</option>
              <option>Atacante</option>
              <option>Goleiro</option>
              <option>Zagueiro</option>
              <option>Centro-avante</option>
              <option>Laterais</option>
          </select></td>
          <td>???</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>
