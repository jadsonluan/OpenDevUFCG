<template>
  <section class="sessao">
    <div class="sessao-head">
      <span class="sessao-titulo">Nossos Projetos</span>
      <span class="sessao-subtitulo">
        Desenvolvemos projetos para a comunidade da UFCG, você também pode contribuir para eles! Veja alguns deles abaixo: 
      </span>
    </div>
    <div class="projetos">
      <ul class="list">
        <li v-for="projeto in projetos" :key="projeto.site" class="list-item">
          <projeto-card :projeto="projeto" />
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
import ProjetoCard from './ProjetoCard.vue'
export default {
  name: 'Projetos',
  components: {
    ProjetoCard
  },
  data() {
    return {
      projetos: [
        {
          titulo: 'Glossário UFCG',
          descricao:
            'Glossário contendo significados de siglas e gírias usadas por alunos da UFCG.',
          site: 'https://glossario.opendevufcg.org/',
          imagem: 'glossario_icon.svg'
        },
        {
          titulo: 'Tamburetei',
          descricao:
            'Repositório contendo materiais para ajudar alunos fazerem de tamburete cadeiras de Computação@UFCG.',
          site: 'https://github.com/opendevufcg/Tamburetei/',
          imagem: 'tamburetei_icon.svg'
        },
        {
          titulo: 'IssueAi',
          descricao:
            'O Issue Ai cria um espaço de visibilidade para os projetos open source de Computação@UFCG.',
          site: 'https://issueai.opendevufcg.org/',
          imagem: 'issueai_icon.svg'
        },
        {
          titulo: 'Roadmap CC',
          descricao: 'Roadmap para se tornar um cientista de Computação@UFCG.',
          site: 'http://roadmap.opendevufcg.org/',
          imagem: 'roadmapcc_icon.svg'
        },
        {
          titulo: 'Laguinho API',
          descricao:
            'Onde todos os dados, pessoas e radiação da UFCG se encontram.',
          site: 'https://github.com/OpenDevUFCG/laguinho-api',
          imagem: 'laguinho_icon.svg'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
.projetos {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin: 0 10vh;
}

.list {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.list-item {
  display: flex;
  widows: 100%;
  flex-direction: row;
  margin: 10px 10px 0 10px;
}

@media only screen and (max-width: 728px) {
  .projetos {
    width: 90vw;
    margin: 10px 10px;
  }
}
</style>
