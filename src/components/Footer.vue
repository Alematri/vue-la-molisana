<script>

  import mainMenu from '../data/mainMenu';
  import { menuProdotti, menuPastificio} from '../data/footerMenu';

  export default{
  name: 'Footer',
  data(){
    return{
      mainMenu,
      menuPastificio,
      menuProdotti
    }
  }
}
</script>

<template>
  <footer>
    <div class="top container">
      <img class="logo" src="/logo-molisana.png" alt="Logo Molisana">

      <nav>
        <h4>Menu</h4>
        <ul>
          <li
          v-for="(item, index) in mainMenu"
          :key="index"
          ><a :href="item.href">{{item.text}}</a></li>
        </ul>
      </nav>

      <nav>
        <h4>pastificio</h4>
        <ul>
          <li
          v-for="(item, index) in menuPastificio"
          :key="index"
          ><a :href="item.href">{{item.text}}</a></li>
        </ul>
      </nav>

      <nav>
        <h4>prodotti</h4>
        <ul>
          <li
          v-for="(item, index) in menuProdotti"
          :key="index"
          ><a :href="item.href">{{item.text}}</a></li>
        </ul>
      </nav>

    </div>

    <div class="bottom">
      <img src="../assets/footer.jpg" alt="Montagne">
    </div>
  </footer>
</template>

<style lang="scss" scoped>

 @use'../scss/partials/variabiles.scss' as *;
  
  footer{
    .top{
      display: flex;
      justify-content: space-between;
      .logo{
        width: 30%;
      }
      h4{
        text-transform: uppercase;
        margin-bottom: 15px;
      }
      li{
        margin-bottom: 10px;
        a{
          color: $link-color;
          font-size: .9rem;
          &:hover{
            text-decoration: underline;
          }
        }
      }
    }
  }

</style>