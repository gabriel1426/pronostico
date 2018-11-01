<template>
<DefaultLayout>
  <section  class="todo">
  <nav class="navbar colornav p-0">
  <a class="navbar-brand">
      <img src='../../assets/logo.png' alt=""> 
  </a>
  <ul class="nav pull-xs-right ">
  <li class="nav-item text-muted p-0">

  <button type="button" class="btn btn-outline-secondary">Iniciar Sesion</button>
  </li>
  <li class="nav-item text-muted">

  <button type="button" class="btn btn-outline-secondary">Registro</button>
  </li>
  </ul>
  </nav>
  <div  class="">
  <div class="row flex-xl-nowrap">

  <div class="col-12 col-md-3 col-xl-2 bd-sidebar fondocolor  p-0">

    <b-nav vertical class="w-100 p-0">
  <ul class="list-group pl-3">
  
  <li class="list-group-item  p-3 lista"><i class="fas fa-home"></i>&nbsp;&nbsp; Predicciones</li>
  <li class="list-group-item  p-3 lista"><i class="fas fa-futbol"></i> &nbsp;&nbsp;Futball</li>
  <li class="list-group-item  p-3 lista"><i class="fas fa-chess"></i>&nbsp;&nbsp;Ajedrez</li>
  <li class="list-group-item  p-3 lista"><i class="fas fa-basketball-ball"></i>&nbsp;&nbsp; Basketball</li>
  <li class="list-group-item  p-3 lista"><i class="fas fa-paw"></i>&nbsp;&nbsp;Carrera de galgos</li>
</ul>
</b-nav>

    </div>
            
    <main class="col-12  col-md-9 col-xl-10 p-0  fond1">
        
    <template>
  <div  class="mh-100"  style="max-height:200px;">
    <b-carousel id="carousel1"
                style="text-shadow: 1px 1px 2px #333;"
                controls
                indicators
                background="#ababab"
                :interval="4000"
                img-max-width="1024"
                img-max-height="200"
                v-model="slide"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >

      <!-- Text slides with image -->
      <b-carousel-slide caption="First slide"
                        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
                        img-src="https://blog.rockthetraveller.com/wp-content/uploads/2017/11/Los-estadios-de-f%C3%BAtbol-m%C3%A1s-incre%C3%ADbles-del-planeta-slider.jpg"
                        class="mh-100"  style="max-height:200px;"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src='http://www.smoothiekingcenter.com/assets/img/tulane-slider-aef3ce1a60.jpg'>
        <h1>Hello world!</h1>
      </b-carousel-slide>

     
    </b-carousel>

  </div>
</template>

        <div class="row flex-xl-nowrap m-2">

        <div class="col-12  col-md-9 col-xl-8 container p-2  ">
  
<div>
    <b-card no-body
            style="max-width: 100%;"
      
            
            img-top>
        
        <h6 slot="header" style="text-align:right"> bookmakers  <b-btn v-b-toggle.collapse1 variant="primary">Comentarios</b-btn> &nbsp;&nbsp; <a href="#">Seguir</a></h6>
        <b-card-body align-self="center" class="p-0" style="text-align: center">

            <b-row >
              <b-col  cols="4">
                <b-img rounded="circle"  width="75" height="75" src="https://sistemas.com/termino/wp-content/uploads/Usuario-Icono.jpg" alt="img" class="m-0 p-0" /> <h5>Gabriel Contreras</h5>
              </b-col>
              <b-col class="vl" cols="8">
                 <h6 <b-img rounded="circle"  width="70" height="70" src="https://winphonemetro.com/wp-content/blogs.dir/26/files/2013/08/Liga-de-F%C3%BAtbol-Profesional.jpg" alt="img" class="m-2 p-2" />
                  España - España Cup Racing Santander - Real Betis</h6>
                  <h3>&nbsp;&nbsp; 3 &nbsp;- &nbsp; 2&nbsp;&nbsp; </h3>
              </b-col>
            </b-row>
      <hr class="m-1">
          <div class="p-0" style="text-align: left">
        
          <b-collapse id="collapse1" class="mt-2">
            <b-card>
              <b-btn v-b-toggle.collapse1_inner size="sm">Comentar</b-btn>
              <b-collapse id=collapse1_inner class="mt-2">
                <b-form-input v-model="text1"
                          type="text"
                          placeholder="Escribe tu comentario"></b-form-input>
                
              </b-collapse>
              <br>
              <b-card>Comentarios</b-card>
              <br>
              
            </b-card>
          </b-collapse>
        </div>
                </b-card-body>
               
                <b-card-footer style="text-align:right">1 de noviembre del 2018</b-card-footer>
                
            </b-card>
        </div>

        </div>
        <div class="col-12  col-md-9 col-xl-4 ">

        </div>
        </div>
    </main>

        </div>
    </div>
    
   
</section>

	</DefaultLayout>

</template>
<script>
export default {
    name:'Home',
     data () {
    return {
      slide: 0,
      sliding: null
    }
  },
   methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>
<style>

.colornav{
  background: rgba(61,61,67,1);
background: -moz-linear-gradient(top, rgba(61,61,67,1) 0%, rgba(61,61,67,1) 38%, rgba(89,89,100,1) 100%);
background: -webkit-gradient(left top, left bottom, color-stop(0%, rgba(61,61,67,1)), color-stop(38%, rgba(61,61,67,1)), color-stop(100%, rgba(89,89,100,1)));
background: -webkit-linear-gradient(top, rgba(61,61,67,1) 0%, rgba(61,61,67,1) 38%, rgba(89,89,100,1) 100%);
background: -o-linear-gradient(top, rgba(61,61,67,1) 0%, rgba(61,61,67,1) 38%, rgba(89,89,100,1) 100%);
background: -ms-linear-gradient(top, rgba(61,61,67,1) 0%, rgba(61,61,67,1) 38%, rgba(89,89,100,1) 100%);
background: linear-gradient(to bottom, rgba(61,61,67,1) 0%, rgba(61,61,67,1) 38%, rgba(89,89,100,1) 100%);
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#3d3d43', endColorstr='#595964', GradientType=0 );
}
.fondocolor{
  background-color:#2a2a2e;
}
.btn{
    margin: 10px;
}
.btn.fin{
    margin-right:60px;
}
.vl {
    border-left: 1px solid #2a2a2e;
    height: 100%;
}
.btn-outline-secondary{
  color: white;
}
li:hover{
  background-color: slategray;
}

.lista{
  background-color: #2a2a2e;
  color:white;
}

.dimensiones{

    width: 100%;
    
}
.todo{
background: rgba(226,226,226,1);
background: -moz-linear-gradient(top, rgba(226,226,226,1) 0%, rgba(219,219,219,1) 31%, rgba(209,209,209,1) 57%, rgba(254,254,254,1) 100%);
background: -webkit-gradient(left top, left bottom, color-stop(0%, rgba(226,226,226,1)), color-stop(31%, rgba(219,219,219,1)), color-stop(57%, rgba(209,209,209,1)), color-stop(100%, rgba(254,254,254,1)));
background: -webkit-linear-gradient(top, rgba(226,226,226,1) 0%, rgba(219,219,219,1) 31%, rgba(209,209,209,1) 57%, rgba(254,254,254,1) 100%);
background: -o-linear-gradient(top, rgba(226,226,226,1) 0%, rgba(219,219,219,1) 31%, rgba(209,209,209,1) 57%, rgba(254,254,254,1) 100%);
background: -ms-linear-gradient(top, rgba(226,226,226,1) 0%, rgba(219,219,219,1) 31%, rgba(209,209,209,1) 57%, rgba(254,254,254,1) 100%);
background: linear-gradient(to bottom, rgba(226,226,226,1) 0%, rgba(219,219,219,1) 31%, rgba(209,209,209,1) 57%, rgba(254,254,254,1) 100%);
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#e2e2e2', endColorstr='#fefefe', GradientType=0 );
}


.bg-light{
  background: #2a2a2e;
  background-color: transparent!important;
}


</style>

