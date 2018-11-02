<template>
<DefaultLayout>
  <section  class="todo">
  <nav class="navbar colornav p-0" >
  <a class="navbar-brand">
      <img src='../../assets/logo.png' alt=""> 
  </a>
  <ul class="nav pull-xs-right ">
  <li class="nav-item text-muted p-0">
    <b-btn v-b-modal.modallogin>Iniciar Sesion</b-btn>
    <b-modal  id="modallogin" title="Ingreso">
    <p class="my-4">Hello from modal!</p>
    <div class="pad" slot="modal-footer" >
         <b-btn size="sm" class="float-right" variant="primary" @click="show=false">
           Enviar
         </b-btn>
       </div>
  </b-modal>
  </li>
  <li class="nav-item text-muted">
   <b-btn v-b-modal.modalregistro>Iniciar Sesion</b-btn>
   <b-modal id="modalregistro" title="Registro">
    <p class="my-4">Hello from modal!</p>
  </b-modal>
  </li>
  </ul>
  </nav>

  <div  class="container">

  <div class="row flex-xl-nowrap">

  <div class="col-12 col-md-3 col-xl-2 bd-sidebar fondocolor p-0">

    <b-navbar vertical class="w-100 p-0" toggleable="md">
    <b-navbar-toggle   target="nav_collapse"></b-navbar-toggle>
     <b-collapse class="" is-nav id="nav_collapse">
       
      <b-list-group class="w-100  p-0">
        <b-list-group-item href="#" button class="lista p-3 listas"><i class="fas fa-home"></i>&nbsp;&nbsp; Predicciones</b-list-group-item>
        <b-list-group-item href="#" button class="lista p-3 listas"><i class="fas fa-futbol"></i> &nbsp;&nbsp;football</b-list-group-item>
        <b-list-group-item href="#" button class="lista p-3 listas"><i class="fas fa-chess"></i>&nbsp;&nbsp;Ajedrez</b-list-group-item>
        <b-list-group-item href="#" button class="lista p-3 listas"><i class="fas fa-basketball-ball"></i>&nbsp;&nbsp; Basketball</b-list-group-item>
        <b-list-group-item href="#" button class="lista p-3 listas"><i class="fas fa-paw"></i>&nbsp;&nbsp;Carrera de galgos</b-list-group-item>
      </b-list-group>

    </b-collapse>
   </b-navbar>

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
      <b-carousel-slide caption="Bienvenidos Ganadores"
                        text="Portal web creado con la ultima  tecnologia, para que ud crezca en grande"
                        img-src="https://blog.rockthetraveller.com/wp-content/uploads/2017/11/Los-estadios-de-f%C3%BAtbol-m%C3%A1s-incre%C3%ADbles-del-planeta-slider.jpg"
                        class="mh-100"  style="max-height:200px;"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src='https://assets.metrolatam.com/ec/2017/02/21/futbol-copa-facebook-1200x600.jpg'>
        <h3>Los Mejores Pronosticos</h3>
      </b-carousel-slide>
       <b-carousel-slide img-src='https://www.jazzdeportes.com/img/products/livedealer.jpg'>
        <h5>Experimenta la tecnologia avanzada y las mejores formulas</h5>
      </b-carousel-slide>

    </b-carousel>

  </div>
</template>

<div class="row flex-xl-nowrap m-2">

  <div class="col-12  col-md-9 col-xl-9 container p-2 ">

      <div class="m-2">
    <b-card no-body
            style="max-width: 100%;"
            img-top>
        <b-card-header class="p-0 pr-3">
        <h6  class="m-0"style="text-align:right"> bookmakers  <b-btn v-b-toggle.collapse1 variant="outline-success">Comentarios</b-btn>
         <b-btn variant="outline-success">seguir</b-btn></h6>

        </b-card-header>
        
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
               
                <b-card-footer style="text-align:right"><i class="far fa-comments" style='font-size:28px;color:white'> </i> &nbsp;&nbsp;1 de noviembre del 2018</b-card-footer>
                
            </b-card>
        </div>


    <div class="card text-center m-2">
        <div class="card-header text-right header">
          bookmakers
        </div>
      <div class="card-body cuerpomensaje ">
       <h5 class="card-title">Tips luke</h5>
       <p class="card-text">España - Copa de España CF Villanovense - Sevilla.</p>
       <a href="#" class="btn btn-primary">Comentar.</a>
      </div>
          <div class="card-footer  text-left header ">
            
             <div class="card-footer  header ">
              <a href=""><i class="far fa-comments" style='font-size:28px;color:white'> </i></a> &nbsp;&nbsp;1 days ago 
          </div> 
          </div>
          
   </div>

  <div class="card text-center m-2">
        <div class="card-header text-right header">
          bookmakers
        </div>
      <div class="card-body cuerpomensaje ">
       <h5 class="card-title">Tips AlbeiroJunior</h5>
       <p class="card-text">España - Copa de España CF Villanovense - Sevilla.</p>
       <a href="#" class="btn btn-primary">Comentar.</a>
      </div>
          <div class="card-footer  text-left header ">
            
             <div class="card-footer  header ">
              <a href=""><i class="far fa-comments" style='font-size:28px;color:white'> </i></a> &nbsp;&nbsp;2 days ago 
          </div> 
          </div>
          
   </div>


        </div>

    <div class="col-12 col-md-3 col-xl-3 bd-sidebar fondocolor fondocolorDerecha  p-0">

        <b-list-group class="w-100  p-0">

        <b-list-group-item class="seccionDerecha p-3"><i class="fas fa-home"></i>&nbsp;&nbsp; Top Bookmakers</b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas"> Coolbet&nbsp;&nbsp;&nbsp;&nbsp;  <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas">Bet365t&nbsp;&nbsp;&nbsp;&nbsp; <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas"> PinnAclet&nbsp;&nbsp;&nbsp; <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas">Sbobet&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas">Coolbet&nbsp;&nbsp;&nbsp;&nbsp; <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i> <i class="far fa-star"></i></b-list-group-item>
        <b-list-group-item href="#" button class="seccionDerecha1 p-3 listas">Betfair&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i> </b-list-group-item>

        </b-list-group>

    

  </div>

        </div>
    </main>

        
    </div>
    
 </div> <!-- fin dic container  -->
</section>






<!-- ffooter  -->
  <div class="container-fluid" style="height: 200px; background: #000;" >
    <div class="container">


       <div class="row">
  <div class="col-md-4">
<h5 class="card-title"  style="color: #ffffff;" >Contactanos</h5>
                <p class="card-text"  style="color: #ffffff;">With supporting text below as a natural lead-in to additional content.</p>
</div>
  <div class="col-md-4">
   <h5 class="card-title"  style="color: #ffffff;">Nuestros apoyos</h5>
                <p class="card-text" style="color: #ffffff;">With supporting text below as a natural lead-in to additional content.</p> 

  </div>
  <div class="col-md-4">
   <h5 class="card-title"  style="color: #ffffff;">Nuestros apoyos</h5>
                <p class="card-text" style="color: #ffffff;">With supporting text below as a natural lead-in to additional content.</p> 

  </div>


  
</div>
    </div>

    

  </div>

    <footer class="py-4 bg-dark">

      <div class="container">
        <p class="m-0 text-center text-white">Copyright &copy; Your Website 2018</p>
      </div>
      <!-- /.container -->
    </footer>

    <!-- fin de footer  -->

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
.fondocolorDerecha{
  background-color:transparent;

}
.btn{
    margin: 10px;
}
button.listas:hover{
   background-color: slategray;
}
.btn.fin{
    margin-right:60px;
}
.btn-outline-secondary{
  color: white;
}

.modal-footer{
  padding: 0%;
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

.seccionDerecha{
  background-color: #ff7f50;
  margin-top: 20px;
  color:white;
}
.seccionDerecha1{
  background-color: #bfece9;
  display: inline-block;
  color:blue;
  font-weight: bold;
}

.card-header{
  background-color:#133337;
  color:white;
}
.card-footer{
  background-color:#133337;
  color:white;
}
.card-body{
  background-color: #f5f5dc;
  
}

</style>

