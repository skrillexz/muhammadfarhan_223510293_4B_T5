<template>
  <q-layout view="hHh lpR fFf">

    <q-header class="bg-black text-white" elevated height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title>
          <q-avatar>
            <img src="gambar/logo1.png">
          </q-avatar>
          Xbox Shop
        </q-toolbar-title>

        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="Home Page" />
        <q-route-tab to="/page2" label="Kart page" />
        <q-route-tab to="/page3" label="Account" />
      </q-tabs>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <div>
    <img src="gambar/lf1.png" style="width: 100%; height: 200%;">
     </div>
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      <div class="q-pa-md">
  <div class="row items-start q-gutter-md">
    <q-card flat bordered class="col">
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label>m.ffarhannn</q-item-label>
          <q-item-label caption>
            Koju
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />

      <q-responsive :ratio="16/20">
        <!-- notice "border-radius-inherit" below; it's important when in a QCard -->
        <q-card-section class="border-radius-inherit flex flex-center flex-column">
          <div>
            <p>GAME YANG DIMILIKI.</p>
          </div>
          <div>
            <img src="gambar/GG1.png" alt="Quasar Logo" style="max-width: 100%;">
          </div>
        </q-card-section>
      </q-responsive>
    </q-card>
  </div>
</div>



    </q-drawer>

    <q-page-container>
      
      <div class="q-pa-md">
        <q-carousel
          animated
          v-model="slide"
          arrows
          navigation
          infinite
        >
          <q-carousel-slide :name="1" img-src="gambar/gambar1.jpg" />
          <q-carousel-slide :name="2" img-src="gambar/gambar2.png" />
          <q-carousel-slide :name="3" img-src="gambar/gambar3.png" /> 
        </q-carousel>
      </div>
      
      <!-- Tulisan di bawah carousel -->
      <div class="text-center" style="text-transform: capitalize; font-weight: bold; font-size: 45px;">
        All Xbox Consoles
      </div>

      <!-- Container untuk kotak-kotak -->
      <div class="q-pa-md row items-start q-gutter-md justify-start">
        <!-- Kotak Xbox -->
        <q-card class="my-card" flat bordered style="width: 250px;">
          <q-img
            src="gambar/xbox1.png"
            style="width: 100%; height: 100%; object-fit: cover;"
          />

          <q-card-section>
            <div class="text-overline text-orange-9">Overline</div>
            <div class="text-h5 q-mt-sm q-mb-xs">Xbox Series S</div>
            <div class="text-caption text-grey">
              Harga terjangkau,
              Desain kompak,
              Memainkan game next-gen dengan kualitas baik dan
             dengan harga Rp.4.786.500
            </div>
          </q-card-section>

          <q-card-actions>
            <q-space />
            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="expanded">
              <q-separator />
              <q-card-section class="text-subtitle2">
                {{ lorem }}
              </q-card-section>
            </div>
          </q-slide-transition>
        </q-card>

        <!-- Kotak 2 -->
        <q-card class="my-card" flat bordered style="width: 250px;">
          <q-img
            src="gambar/xbox2.png"
            style="width: 100%; height: 100%; object-fit: cover;"
          />

          <q-card-section>
            <div class="text-overline text-orange-9">Overline</div>
            <div class="text-h5 q-mt-sm q-mb-xs">Xbox Series S-1TB</div>
            <div class="text-caption text-grey">
              Harga terjangkau,
              Desain kompak,
              ukuran 1TB
              di bandrol dengan harga Rp.5.568.295
            </div>
          </q-card-section>

          <q-card-actions>
            <q-space />
            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="expanded">
              <q-separator />
              <q-card-section class="text-subtitle2">
                {{ lorem }}
              </q-card-section>
            </div>
          </q-slide-transition>
        
        </q-card>

        <!-- Kotak 3 -->
        <q-card class="my-card" flat bordered style="width: 250px;">
          <q-img
            src="gambar/xbox3.png"
            style="width: 100%; height: 100%; object-fit: cover;"
          />

          <q-card-section>
            <div class="text-overline text-orange-9">Overline</div>
            <div class="text-h5 q-mt-sm q-mb-xs">Xbox Series X</div>
            <div class="text-caption text-grey">
              Harga terjangkau,
              Desain kompak,
              di bandrol dengan harga Rp.7.163.795
            </div>
          </q-card-section>

          <q-card-actions>
            <q-space />
            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="expanded">
              <q-separator />
              <q-card-section class="text-subtitle2">
                {{ lorem }}
              </q-card-section>
            </div>
          </q-slide-transition>
        </q-card>

        <!-- Kotak 4 -->
        <q-card class="my-card" flat bordered style="width: 250px;">
          <q-img
            src="gambar/xbox4.png"
            style="width: 100%; height: 100%; object-fit: cover;"
          />

          <q-card-section>
            <div class="text-overline text-orange-9">Overline</div>
            <div class="text-h5 q-mt-sm q-mb-xs">Xbox Series S (certifed)</div>
            <div class="text-caption text-grey">
              Harga terjangkau,
              Desain kompak,
             dibandrol dengan harga Rp.6.844.695
            
            </div>
          </q-card-section>

          <q-card-actions>
            <q-space />
            <q-btn
              color="grey"
              round
              flat
              dense
              :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
              @click="expanded = !expanded"
            />
          </q-card-actions>

          <q-slide-transition>
            <div v-show="expanded">
              <q-separator />
              <q-card-section class="text-subtitle2">
                {{ lorem }}
              </q-card-section>
            </div>
          </q-slide-transition>

        </q-card>
      </div>

        
        
          
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
          </q-avatar>
          <div>Title</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      slide: ref(1),
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
</style>
