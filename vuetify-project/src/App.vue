 <!-- Cabecalho/Header -->
 <template>
  <v-app theme="light">

    <!-- Navegação -->
    <v-navigation-drawer v-model="isDrawerOpen">
      <v-list>
        <v-list-subheader>Menu</v-list-subheader>
        <v-list-item prepend-icon="mdi-home">Home</v-list-item>
        <v-list-item prepend-icon="mdi-phone">Contato</v-list-item>
      <v-list-group value="Viagens">
        <template #activator="{props}">
          <v-list-item v-bind="props" prepend-icon="mdi-airplane">Viagens</v-list-item>
        </template>
        <v-list-item prepend-icon="mdi-passport">Destinos</v-list-item>
        <v-list-item prepend-icon="mdi-package-variant">Pacotes de Viagens</v-list-item>
        <v-list-item prepend-icon="mdi-bed-outline">Reservas</v-list-item>
        <v-list-item prepend-icon="mdi-gift-outline">Promoções Especiais</v-list-item>
        <v-list-item prepend-icon="mdi-human-greeting">Guias de Viagem</v-list-item>
        <v-list-item prepend-icon="mdi-account-voice">Idioma</v-list-item>
        <v-list-item prepend-icon="mdi-currency-usd">Moeda</v-list-item>
        <v-list-item prepend-icon="mdi-information">Sobre</v-list-item>
      </v-list-group>
    </v-list>
    </v-navigation-drawer>

    <!-- Nav-bar e nome do site -->
    <v-app-bar flat class="border-b">
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>
      <v-app-bar-title>World Travels</v-app-bar-title>
      

      <!-- Foto de perfil -->
      <template #append>
        <v-menu >
          <template v-slot:activator="{ props }">
        <v-btn  prepend-icon="mdi-account" v-bind="props">Usuário</v-btn>
      </template>
      <v-list>
        <v-list-item  prepend-icon="mdi-login" class="cursor-pointer" @mouseover="loginHover = true"
        @mouseleave="loginHover = false"
        :class="{ 'v-list-item--active': loginHover }">Login</v-list-item>
        <v-list-item  prepend-icon="mdi-account-plus-outline" class="cursor-pointer" @mouseover="cadastroHover = true"
        @mouseleave="cadastroHover = false"
        :class="{ 'v-list-item--active': cadastroHover }">Cadastrar</v-list-item>
      </v-list>
        </v-menu>

        <!-- Notificação -->
         <v-menu>
          <template #activator="{props}">
            <v-btn v-bind="props" icon class="mr-2">
              <v-badge dot color="info">
                <v-icon icon="mdi-bell-outline"></v-icon>
              </v-badge>
            </v-btn>
          </template>
          <v-card min-width="150px">
            <v-list :lines="false" density="compact" nav>
              <v-list-item prepend-icon="mdi-bell-outline">
                <v-list-item-title>Notificações</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-card>
         </v-menu>

        <!-- Adicionar Meu perfil na foto -->
      <v-menu>
        <template #activator="{props}">
          <v-avatar v-bind="props">
            <v-img cover src="https://s3.amazonaws.com/video-api-ai/system/tool/talking_head/657acc0f37d42.jpg"></v-img>
          </v-avatar>
        </template>
        <v-card min-width="200px">
          <v-list :lines="false" density="comapact" nav>
            <v-list-item prepend-icon="mdi-account-outline">
              <v-list-item-title>Meu perfil</v-list-item-title>
            </v-list-item>
            <v-list-item prepend-icon="mdi-heart-outline">
              <v-list-item-title>Viagens favoritas</v-list-item-title>
            </v-list-item>
            <v-list-item prepend-icon="mdi-credit-card-outline">
              <v-list-item-title>Pagamentos</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-menu>
      </template>
    </v-app-bar>
    
    <!-- Começo dos destinos -->
    <v-main>
      <v-container>
        <h1 class="mb-4">Dashboard</h1>

        <v-card flat class="border mb-4">
          <v-card-title>Ultimos</v-card-title>
          <v-table density="compact">
            <t-head>
              <tr>
                <th></th>git remote -v

              </tr>
            </t-head>
              <t-body>
                <tr class="border-b-">
                  <td>teste</td>
                </tr>
                <tr>
                  <td>teste</td>
                </tr>
              </t-body>
          </v-table>
        </v-card>
        <h1>Europa</h1>
        <v-row>
          <!-- ITÁLIA -->
           <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img src="https://cdn.pixabay.com/photo/2021/07/24/15/47/venice-6489813_1280.jpg" class="align-end text-white">
                <v-card-title>Veneza</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Itália</v-card-subtitle>
              <v-card-text>
                <div>
                  Descubra a encantadora Veneza, Itália - a cidade das águas. Com sua arquitetura deslumbrante e canais serpenteantes, cada esquina revela tesouros artísticos e a autenticidade da culinária local. Em Veneza, cada passo é uma descoberta e cada canal uma história.
                </div>
              </v-card-text>

              <!-- Ver mais -->
              <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon center>mdi-eye</v-icon>Ver mais
                </v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar
                </v-btn>
                  
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- FRANÇA -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://cdn.pixabay.com/photo/2019/07/21/16/29/paris-4353082_1280.jpg" class="align-end text-white">
                <v-card-title>Paris</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">França</v-card-subtitle>
              <v-card-text>
                <div>
                    Descubra a deslumbrante Paris, França, a cidade da luz. Com sua arquitetura icônica e charmosas ruas, cada esquina é um convite à história e à cultura. Em Paris, cada caminhada reserva novas surpresas, cada monumento conta sua própria narrativa.
                </div>
              </v-card-text>
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <!-- ESPANHA -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://cdn.pixabay.com/photo/2022/06/22/16/10/cathedral-7278228_1280.jpg" class="align-end text-white">
                <v-card-title>Barcelona</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Espanha</v-card-subtitle>
              <v-card-text>
                <div>Descubra Barcelona, Espanha - uma cidade vibrante. Com sua arquitetura única e ruas movimentadas, cada esquina oferece uma experiência cultural. Em Barcelona, cada passo revela uma nova história, tornando cada visita memorável e cheia de surpresas</div>
              </v-card-text>
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <!-- Alemanha -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://cdn.pixabay.com/photo/2017/07/28/00/03/thuringia-germany-2547256_1280.jpg" class="align-end text-white">
                <v-card-title>Turíngia</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Alemanha</v-card-subtitle>
              <v-card-text>
                <div>Descubra Turingia, Alemanha - história e natureza. Cada canto revela cultura e beleza natural. Cada passo, uma nova história para desvendar. Explore esta região encantadora e deixe-se surpreender a cada momento. Dos castelos imponentes às trilhas serenas.</div>
              </v-card-text>
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <!-- América do Sul -->
          <!-- Brasil -->
          <v-container>
            <h1>América do Sul</h1>
            <v-row>
              <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/6580703/pexels-photo-6580703.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Rio de Janeiro</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Brasil</v-card-subtitle>
              <v-card-text>
                <div>O Rio de Janeiro, "Cidade Maravilhosa", é famoso por suas praias e pontos turísticos icônicos, como o Pão de Açúcar e o Cristo Redentor. Com uma rica história cultural e o vibrante carnaval, o Rio atrai milhões de visitantes anualmente.</div>
              </v-card-text>
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Brasil -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/18025862/pexels-photo-18025862/free-photo-of-cidade-meio-urbano-carros-veiculos.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>São Paulo</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Brasil</v-card-subtitle>
              <v-card-text>
                <div>São Paulo, a maior cidade do Brasil, é um centro cosmopolita de cultura, negócios e entretenimento. Conhecida por sua diversidade gastronômica, vida noturna agitada e arquitetura impressionante, oferece uma experiência urbana única. Com uma rica cena artística e cultural.
                </div>
              </v-card-text>
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Argentina -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/22690629/pexels-photo-22690629/free-photo-of-cidade-meio-urbano-carros-veiculos.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Buenos Aires</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Argentina</v-card-subtitle>
              <v-card-text>
                <div>Buenos Aires, a capital da Argentina, é uma cidade que mistura charme europeu com paixão latina. Conhecida por seus bairros distintos, como o colorido La Boca e o elegante Recoleta, oferece uma rica experiência cultural. De seus icônicos cafés e restaurantes.</div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Chile -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/19821195/pexels-photo-19821195/free-photo-of-cidade-meio-urbano-ponto-de-referencia-ponto-historico.jpeg" class="align-end text-white">
                <v-card-title>Santiago</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Chile</v-card-subtitle>
              <v-card-text>
                <div>Santiago, capital do Chile, é uma cidade moderna nos Andes, com arquitetura contemporânea e uma cena gastronômica vibrante. Rica em cultura e natureza, oferece museus de destaque, vida noturna animada e acesso fácil a atividades ao ar livre, com sua diversidade e beleza.
                </div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 
            </v-row>
          </v-container>

          <!-- América do Norte -->
          <v-container>
            <h1>América do Norte</h1>
            <v-row>
              <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/5847766/pexels-photo-5847766.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Nova York</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Estados Unidos</v-card-subtitle>
              <v-card-text>
                <div>Nova York, a cidade icônica que nunca dorme, é um centro de cultura, negócios e diversão. Com sua deslumbrante linha do horizonte, teatros da Broadway, restaurantes de classe mundial e atrações como a Estátua da Liberdade, oferece uma experiência única para os viajantes.</div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Estados Unidos -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/16306377/pexels-photo-16306377/free-photo-of-cidade-meio-urbano-carros-veiculos.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Los Angeles</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Estados Unidos</v-card-subtitle>
              <v-card-text>
                <div>
                  Los Angeles, a cidade dos anjos, é o coração da indústria do entretenimento e do estilo de vida descontraído da Califórnia. Com seu clima ensolarado, praias deslumbrantes e famosos pontos turísticos como Hollywood e Beverly Hills. 
                </div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Canada -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/2773225/pexels-photo-2773225.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Toronto</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Canadá</v-card-subtitle>
              <v-card-text>
                <div>Toronto, a cidade cosmopolita do Canadá, combina harmoniosamente cultura, diversidade e modernidade. Com sua deslumbrante linha do horizonte, incluindo a icônica CN Tower, e seus diversos bairros étnicos, oferece uma experiência multicultural única. </div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Canada -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/20482103/pexels-photo-20482103/free-photo-of-cidade-meio-urbano-trafego-transito.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Vancouver</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Canadá</v-card-subtitle>
              <v-card-text>
                <div>
                  Vancouver, na costa oeste do Canadá, é uma fusão deslumbrante de natureza e cidade. Com suas montanhas cobertas de neve, praias pitorescas e parques exuberantes, oferece uma experiência ao ar livre incomparável. Conhecida por sua cultura diversificada.
                </div>
              </v-card-text>

                <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 
            </v-row>
          </v-container>

          <!-- África -->
          <v-container>
            <h1>África</h1>
            <v-row>
              <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/9324233/pexels-photo-9324233.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Cidade do Cabo</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">África do Sul</v-card-subtitle>
              <v-card-text>
                <div> Conhecida por sua incrível diversidade, a África do Sul oferece desde safáris em parques nacionais como o Kruger até cidades vibrantes como Cidade do Cabo e Joanesburgo, com belas praias, vinícolas, e uma rica cultura.</div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Estados Unidos -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/3889918/pexels-photo-3889918.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Tanzânia</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">África</v-card-subtitle>
              <v-card-text>
                <div>
                  Lar do icônico Monte Kilimanjaro e do espetacular Parque Nacional Serengeti, a Tanzânia é um destino popular para safáris, além de oferecer belas praias na ilha paradisíaca de Zanzibar, praias de areias brancas e águas cristalinas
                </div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Canada -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/3061496/pexels-photo-3061496.jpeg" class="align-end text-white">
                <v-card-title>Rabat</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">Marrocos</v-card-subtitle>
              <v-card-text>
                <div>Com cidades fascinantes como Rabat, Fez e Casablanca, Marrocos é conhecido por seus culturais e naturais souks (mercados), palácios exóticos, paisagens deslumbrantes no deserto do Saara e nas montanhas do Atlas.  </div>
              </v-card-text>

              <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 

          <!-- Canada -->
          <v-col cols="12" md="4" lg="3">
            <v-card>
              <v-img src="https://images.pexels.com/photos/7566890/pexels-photo-7566890.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" class="align-end text-white">
                <v-card-title>Egito</v-card-title>
              </v-img>
              <v-card-subtitle class="pt-3">África</v-card-subtitle>
              <v-card-text>
                <div>
                  Lar das pirâmides de Gizé, o Egito oferece uma rica história antiga, com templos, tumbas e artefatos fascinantes ao longo do rio Nilo, além de praias no Mar Vermelho e no Mar Mediterrâneo oferecem oportunidades para mergulho.
                </div>
              </v-card-text>

                <!-- Ver mais -->
               <v-card-actions class="d-flex justify-space-between px-3"> 
                <v-btn variant="outlined" color="primary">
                  <v-icon left>mdi-eye</v-icon> Ver mais</v-btn>

                  <!-- Comprar -->
                <v-btn variant="tonal" color="primary">
                  <v-icon left>mdi-cart</v-icon> Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col> 
            </v-row>
          </v-container>


          <!-- Principal -->
        </v-row>    
      </v-container>
    </v-main>
  </v-app>
 </template>

<script setup> 
 import { ref } from 'vue'
 const isDrawerOpen = ref(false)
 const loginHover = ref(false)
 const cadastroHover = ref(false)
</script>

<style>
  
</style>
