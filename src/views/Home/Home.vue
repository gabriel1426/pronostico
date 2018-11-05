<template>
<DefaultLayout>
  <section  class="todo">
    <nav class="navbar colornav p-0" >
      <a class="navbar-brand ">
        <img class="padLogo" src='../../assets/logo.png' alt=""> 
      </a>
      <ul class="nav pull-xs-right ">
        <li class="nav-item text-muted p-0">
          
          <div class="text-center">
            
              <button  type="button" class="btn btn-outline-info  listas" data-toggle="modal" data-target="#membreciaModal"  @click="cambiar('login')">
                  Ingresar
              </button>
              <button type="button" class="btn btn-outline-info  listas" data-toggle="modal" data-target="#membreciaModal"  @click="cambiar('membresia')">
                  Membresía
              </button>
          </div>
          
          <div class="modal fade" id="membreciaModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
              <div class="modal-dialog m-0 h-100 mh-100 w-100 position-fixed" role="document">
                  <div class="modal-content h-100 rounded-0">
                    <div class="modal-header colornav">
                          <h3>Ingresa</h3>
                    </div>
                    <div class="modal-body">
                        <div v-if= "login" class="nav flex-sm-column flex-row">
                          <div v-if= "login">
                            <div  class="col-12 col-md-12 col-xl-12">
                              <form>
                            <div class="form-group">
                              <label for="correologin">Correo</label>
                              <input v-model = "correo" type="mail" class="form-control" id="correologin" placeholder="Example@example.com"> 
                            </div>
                            <div class="form-group">
                              <label for="clave">Clave</label>
                              <input v-model = "clave" type="password" class="form-control" id="clave" placeholder="****">
                            </div>
                            <button class="btn btn-success text-center" type="submit" v-on:click="" style="text-align: center" >Iniciar Sesión</button>
                            </form>
                            <hr >
                          </div>
                        <div  class="col-12 md-12 col-xl-12 text-center" >
                          <p >Aun no eres mienbro !Solicita tu membresía¡</p>
                          <br>
                      <button class="btn btn-danger   " type="submit" @click="cambiar('membresia')" style="text-align: center" >Solicitar membresía</button>
                        </div>
                        </div>
                              
                        </div>
                        <div v-else class="nav flex-sm-column flex-row">
                          <div  class="col-12 col-md-12 col-xl-12">
                            <form>
                                <div class="form-group">
                                  <label for="correologin">Correo</label>
                                  <input v-model = "correor" type="mail" class="form-control" id="correologin" placeholder="Example@example.com"> 
                                </div>
                                <div class="form-group">
                                  <label for="correologin">Nombre</label>
                                  <input v-model = "nombrer" type="mail" class="form-control" id="correologin" placeholder="Nombre de usuario"> 
                                </div>
                                <div class="form-group">
                                  <label for="clave">Contraseña</label>
                                  <input v-model = "claver" type="password" class="form-control" id="clave" placeholder="****">
                                </div>
                                <div class="form-group">
                                  <label for="correologin">Confirmar contraseña</label>
                                  <input v-model = "rclaver" type="mail" class="form-control" id="correologin" placeholder="Nombre de usuario"> 
                                </div>
                                <div class="form-group">
                                  <input type="checkbox" id="checkbox" v-model= "aceptarr">
                                  <label for="checkbox">Aceptar terminos y condiciones</label>
                                </div>
                                <button class="btn btn-success " type="submit" v-on:click="" style="text-align: center" >Solicitar membresia</button>
                              </form>
                              </div>
                        </div>
                    </div>
                    <div class="modal-footer colornav">
                        <button type="button" class="btn btn-outline-info" data-dismiss="modal">Close</button>
                    </div>
                  </div>
              </div>
          </div>
        </li>
      </ul>
    </nav>
    <div class="container-fluid">
      <div class="row flex-xl-nowrap">
        <div class="col-12 col-md-3 col-xl-2 bd-sidebar fondocolor p-0">
          <b-navbar vertical class="w-100 p-0" toggleable="md">
            <b-navbar-toggle   target="nav_collapse"></b-navbar-toggle>
            <b-collapse class="" is-nav id="nav_collapse">
              <b-list-group class="w-100  p-0">
                <b-list-group-item href="#" button class="lista pl-20 listas"><i class="fas fa-home"></i>&nbsp;&nbsp; Predicciones</b-list-group-item>
                <b-list-group-item href="#" button class="lista  pl-20 listas"><i class="fas fa-futbol"></i> &nbsp;&nbsp;football</b-list-group-item>
                <b-list-group-item href="#" button class="lista pl-20 listas"><i class="fas fa-chess"></i>&nbsp;&nbsp;Ajedrez</b-list-group-item>
                <b-list-group-item href="#" button class="lista pl-20 listas"><i class="fas fa-basketball-ball"></i>&nbsp;&nbsp; Basketball</b-list-group-item>
                <b-list-group-item href="#" button class="lista pl-20listas"><i class="fas fa-paw"></i>&nbsp;&nbsp;Carrera de galgos</b-list-group-item>
              </b-list-group>
            </b-collapse>
          </b-navbar>
        </div>
        <main class="col-12 col-md-9 col-xl-10 p-0 ">
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
                          @sliding-end="onSlideEnd">
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
          <div class="row flex-xl-nowrap m-2">
            <div class="col-12  col-md-9 col-xl-8 p-2 ">
              <div class="m-2">
                <b-card no-body
                      style="max-width: 100%;"
                      img-top>
                  <b-card-header class="p-0 pr-3">
                  <h6  class="m-0" style="text-align:right"> bookmakers  <b-btn v-b-toggle.collapse1 variant="outline-info">Comentarios</b-btn>
                  <b-btn variant="outline-info">seguir</b-btn></h6>
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
                    <b-collapse id="collapse1" class="mt-2 p-0">
                      <b-card>
                        <b-btn v-b-toggle.collapse1_inner size="sm">Comentar</b-btn>
                        <b-collapse id=collapse1_inner class="mt-2 p-0">
                          <b-form-input 
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
            </div>
            <div class="col-12 col-md-3 col-xl-3 bd-sidebar fondocolor fondocolorDerecha  p-0 container">

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
      </div> <!-- fin dic container  -->
    </div>
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
  </section>
  
</DefaultLayout>
</template>
<script>
export default {
    name:'Home',
     data () {
    return {
      login:true,
      correo:'',
      clave:'',
      correor:'',
      nombrer:'',
      claver:'',
      rclaver:'',
      aceptarr:'',
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
    },
    cambiar(login){
     if (login==="login"){
        this.login=true;
     }else { 
        this.login=false;
     }
    },
    login(){
      
    }
  }
}
</script>
<style>

.colornav{
 background: #09182d ;

}
.fondocolor{
  background-color:#09182d  !important;
}
.fondocolorDerecha{
  background-color:transparent !important;

}
.btn{
    margin: 10px;
}
button.listas:hover{
   background-color: slategray !important;
}
.btn.fin{
    margin-right:60px !important;
}
.btn-outline-secondary{
  color: white !important;
}
.padLogo{
  padding-left: 50px;
}
.modal-footer{
  padding: 0%;
}
.modal-header{
  background-color:#1c344d!important;
  color:white !important;
  border-radius: 0rem !important;
}
.modal-body{
  background-color: #3c546e !important;
  color:white !important;
}
.modal-footer{
  background-color:#1c344d!important;
  color:white !important;
}
.lista{
  background-color: #09182d  !important;
  color:white !important;
}
.todo{
  background-color: #102034;
}
.modallogin{
  background-color: #5d5d6b !important;
  margin-right: 100px;
  color: width;
}
.seccionDerecha{
  background-color:#1c344d!important;
  margin-top: 20px !important;
  color:white !important;
}
.seccionDerecha1{
  background-color: #3c546e !important;
  color:white !important;
  display: inline-block !important;
  
  font-weight: bold!important;
}
.card-header{
  background-color:#09182d !important;
  color:white !important;
}
.card-footer{
  background-color:#09182d!important;
  color:white !important;
}
.card-body{
  background-color: #1c344d !important;
  color:white !important;
 
}
</style>

