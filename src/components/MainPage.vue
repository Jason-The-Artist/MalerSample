<style scoped>

.header-background{
  background: #eef4fc;
}

.header-outer{
  height: 100vh;
}

.header-inner{
  height: 80%;
}

.main-headline{
  font-size: 80px;
}

.half-width{
  width: 50%;
}

.down-icon{
  opacity: 0.5;
  transform: translateY(-60px);
}

.huge-headline{
  font-size: 40px;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.about-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

.us-background{
  background: #f7f8f9;
  padding-top: 100px;
  padding-bottom: 100px;
}

.contact-background{
  background: #111827;
  padding-top: 100px;
  padding-bottom: 100px;
}

.about-half-width{
  width: 50%;
}

.tri-width{
  width: 33%;
}

.address-card{
  width: 500px;
  padding: 20px;
}

.message-card{
  width: 500px;
  padding: 20px;
}

.contact-circle{
  width: 50px;
  height: 50px;
  background: rgb(37, 98, 233);
}

.hide-pizza{
  display: flex;
}

.mobile-center-horizontal{
  display: flex;
}

.mobile-center{
  display: flex;
  align-items: center;
}

.button-space{
  width: 20px;
}

.contact-space{
  width: 20px;
}

.inner-img{
  width: 90%;
}

.main-tag{
  width: fit-content;
  border-radius: 100px;
  padding: 3px;
  padding-left: 6px;
  padding-right: 6px;
  background: #d9e8fc;
  color: #1e3fae;
  font-size: 13px;
  font-weight: bold;
}

.black-tag{
  width: fit-content;
  border-radius: 100px;
  padding: 3px;
  padding-left: 6px;
  padding-right: 6px;
  background: #000000;
  color: white;
  font-size: 13px;
  font-weight: bold;
}


.rating-card{
  width: fit-content;
  height: fit-content;
  padding: 15px;
  border-radius: 10px;
  background: white;
}

.round-icon{
  width: 40px;
  height: 40px;
  border-radius: 200px;
}

.decent-sec-background{
  background: #dafae5;
}

.sec-color{
  color: #16a249;
}

.contact-opening{
  padding: 20px;
  background: #1f2937;
}

.diagonal-line{
  height: 180%;
  width: 35vh;
  rotate: 20deg;
  background: #eef4fc;
  z-index: 100;
  transform: translateX(17vh);
}

.header-content-width{
  width: 100%;
  margin-left: 200px;
}

.main-video{
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.mobile-limit-height{
  height: 100%;
}

@media (max-width: 1450px) {
  .product-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }
}

@media (max-width: 1000px) {
  .hide-pizza{
    display: none;
  }
  .half-width{
    width: 100%;
  }

  .mobile-center-horizontal{
    display: flex;
    justify-content: center;
  }

  .mobile-center-text{
    text-align: center;
  }

  .mobile-center{
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .mobile-column{
    flex-direction: column;
  }

  .diagonal-line{
    display: none;
  }

  .header-content-width{
    margin-left: 0;
    margin-top: 100px;
  }

  .mobile-absolute{
    position: absolute;
  }

  .mobile-limit-height{
    height: 80%;
  }

  .main-video{
    filter: brightness(0.5);
  }

  .mobile-white{
    color: white;
  }

}
@media (max-width: 1060px) {
  .contact-column{
    flex-direction: column;
  }

  .address-card{
    width: 85%;
  }

  .message-card{
    width: 85%;
  }

  .contact-space{
    height: 10px;
  }

  .product-grid {
    grid-template-columns: repeat(1, 1fr);
  }
}

@media (max-width: 600px) {
  .main-headline{
    font-size: 10vw;
  }

  .mobile-button-column{
    flex-direction: column;
  }

  .button-space{
    height: 10px;
  }

  .small-mobile-font{
    font-size: 12px;
  }

}

</style>

<template>

  <Nav class="fade-bottom-before on-top" :class="fadeNav ? 'fade-bottom-after' : ''"/>

  <div class="header-background overflow-hidden header-outer center" id="home">
    <div class="mobile-limit-height max-width space-between relative center-vertical mobile-column">
      <div class="relative mobile-absolute max-height center-vertical right half-width">
        <div class="center-vertical mobile-absolute fade-before" :class="fadeHeader ? 'fade-after' : ''" style="z-index: 200">
          <div class="header-content-width">
            <div class="mobile-center-horizontal">
              <div class="main-tag">Professionelle Malerarbeiten seit 1995</div>
            </div>
            <h1 class="reset-margin main-headline mobile-center-text mobile-white">Ihr Zuhause in <span class="prim-color">neuen Farben</span></h1>
            <p class="default-textsize decent-color mobile-white fade-before mobile-center-text" :class="fadeSubHeader ? 'fade-after' : ''">Wir verwandeln Ihre Räume mit hochwertigen Malerarbeiten, modernen Techniken und jahrzehntelanger Erfahrung.</p>
            <div class="mobile-center-horizontal fade-before mobile-button-column" :class="fadeSubButtons ? 'fade-after' : ''">
              <div class="center-horizontal">
                <UIButton title="Kostenlos beraten lassen" @click="onContact"/>
              </div>
              <div class="button-space"></div>
              <div class="center-horizontal">
                <UIButton title="Unsere Arbeiten ansehen" text-css="mobile-white" sec @click="onProjects"/>
              </div>
            </div>
          </div>
        </div>
        <div class="diagonal-line absolute"></div>
      </div>
      <div class="center half-width relative max-height">
        <div class="absolute center max-width max-height">
          <div class="max-width max-height center">
            <video autoplay loop muted playsinline class="main-video">
              <source src="../assets/maler-video.mp4" type="video/mp4">
            </video>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="center-horizontal down-icon" id="menu">
    <Icon size="40" class="prim-color">
      <ChevronDoubleDown20Regular/>
    </Icon>
  </div>

  <div class="center-horizontal" ref="menu">
    <div class="leistung-content-width center-horizontal">
      <div>
        <div class="center-horizontal">
          <div class="black-tag">Unsere Leistungen</div>
        </div>
        <div class="center-horizontal">
          <h2 class="huge-headline center-text">Professionelle Malerarbeiten für jeden Bedarf</h2>
        </div>
        <div class="center-horizontal">
          <p class="decent-color default-textsize reset-margin center-text">Von der Innenraumgestaltung bis zur Fassadensanierung - wir bieten Ihnen das komplette Spektrum professioneller Malerarbeiten.</p>
        </div>
      </div>
    </div>
  </div>

  <div style="height: 50px"></div>

  <div class="center-horizontal">
    <div class="leistung-content-width center-horizontal">
      <div class="product-grid max-width">
        <LeistungCard title="Innenraumgestaltung" sub="Wände, Decken und Türen in perfekter Qualität" :list="['Wandgestaltung', 'Deckenanstrich', 'Türen & Fenster']"><Icon size="35" class="prim-color"><Home24Regular/></Icon></LeistungCard>
        <LeistungCard title="Fassadenarbeiten" sub="Schutz und Verschönerung Ihrer Außenwände" :list="['Fassadenanstrich', 'Putzarbeiten', 'Wärmedämmung']"><Icon size="35" class="prim-color"><Building24Regular/></Icon></LeistungCard>
        <LeistungCard title="Spezialarbeiten" sub="Kreative Techniken für besondere Ansprüche" :list="['Spachteltechnik', 'Lasurtechnik', 'Dekorputz']"><Icon size="35" class="prim-color"><Color20Regular/></Icon></LeistungCard>
      </div>
    </div>
  </div>

  <div style="height: 50px" id="about"></div>

  <div class="max-width us-background center-horizontal">
    <div class="header-inner main-content-width space-between center-vertical mobile-column">
      <div class="center half-width">
        <div>
          <div class="mobile-center-horizontal">
            <div class="black-tag">Über MalerPro</div>
          </div>
          <h1 class="huge-headline mobile-center-text">Qualität und Erfahrung seit über 25 Jahren</h1>
          <p class="default-textsize reset-margin mobile-center-text decent-color">Als familiengeführtes Unternehmen stehen wir für höchste Qualität, Zuverlässigkeit und persönlichen Service. Unser erfahrenes Team verwirklicht Ihre Wünsche mit modernsten Techniken und hochwertigen Materialien.</p>
          <div style="height: 20px"></div>
          <div class="flex">
            <div class="center-vertical about-half-width">
              <div class="round-icon decent-prim-background center">
                <Icon size="25" class="prim-color">
                  <Clock20Regular/>
                </Icon>
              </div>
              <div style="width: 10px"></div>
              <div>
                <p class="reset-margin bold">Pünktlich</p>
                <div style="height: 5px"></div>
                <p class="reset-margin decent-color" style="font-size: 13px">Termintreue Ausführung</p>
              </div>
            </div>
            <div class="center-vertical about-half-width">
              <div class="round-icon decent-prim-background center">
                <Icon size="25" class="prim-color">
                  <Clock20Regular/>
                </Icon>
              </div>
              <div style="width: 10px"></div>
              <div>
                <p class="reset-margin bold">Pünktlich</p>
                <div style="height: 5px"></div>
                <p class="reset-margin decent-color" style="font-size: 13px">Termintreue Ausführung</p>
              </div>
            </div>
          </div>
          <div style="height: 30px"></div>
          <div class="flex">
            <div class="center-vertical about-half-width">
              <div class="round-icon decent-prim-background center">
                <Icon size="25" class="prim-color">
                  <Clock20Regular/>
                </Icon>
              </div>
              <div style="width: 10px"></div>
              <div>
                <p class="reset-margin bold">Pünktlich</p>
                <div style="height: 5px"></div>
                <p class="reset-margin decent-color" style="font-size: 13px">Termintreue Ausführung</p>
              </div>
            </div>
            <div class="center-vertical about-half-width">
              <div class="round-icon decent-prim-background center">
                <Icon size="25" class="prim-color">
                  <Clock20Regular/>
                </Icon>
              </div>
              <div style="width: 10px"></div>
              <div>
                <p class="reset-margin bold">Pünktlich</p>
                <div style="height: 5px"></div>
                <p class="reset-margin decent-color" style="font-size: 13px">Termintreue Ausführung</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="center half-width">
        <div class="about-grid">
          <img src="../assets/bild2.webp" class="max-width round-corner max-height contain">
          <div class="max-width max-height center"><img src="../assets/bild1.webp" class="max-width round-corner contain"></div>
          <div class="max-width max-height center"><img src="../assets/bild4.webp" class="max-width round-corner contain"></div>
          <img src="../assets/bild3.webp" class="max-width round-corner contain">
        </div>
      </div>
    </div>
  </div>

  <div style="height: 50px" id="projects"></div>

  <div class="center-horizontal" ref="projects">
    <div class="main-content-width center-horizontal">
      <div>
        <div class="center-horizontal">
          <div class="black-tag">Unsere Projekte</div>
        </div>
        <div class="center-horizontal">
          <h2 class="huge-headline center-text">Einige unserer schönsten Arbeiten</h2>
        </div>
        <div class="center-horizontal">
          <p class="decent-color default-textsize reset-margin center-text">Lassen Sie sich von unseren realisierten Projekten inspirieren</p>
        </div>
      </div>
    </div>
  </div>

  <div style="height: 50px"></div>

  <div class="center-horizontal">
    <div class="main-content-width center-horizontal">
      <div class="product-grid max-width">
        <ProjectCard title="Moderne Wohnzimmergestaltung" city="München" tag="Innenraumgestaltung" img="thumb1.jpg" path="/project1"/>
        <ProjectCard title="Fassadensanierung Einfamilienhaus" city="Hamburg" tag="Fassadenarbeiten" img="thumb2.jpg" path="/project2"/>
        <ProjectCard title="Büroräume Neugestaltung" city="Berlin" tag="Gewerblich" img="thumb3.jpg" path="/project3"/>
        <ProjectCard title="Altbau Renovierung" city="Köln" tag="Innenraumgestaltung" img="thumb4.jpeg" path="/project4"/>
        <ProjectCard title="Moderne Küche" city="Frankfurt" tag="Spezialarbeiten" img="thumb5.webp" path="/project5"/>
        <ProjectCard title="Penthouse Gestaltung" city="Stuttgart" tag="Luxus" img="thumb6.webp" path="/project6"/>
      </div>
    </div>
  </div>

  <div style="height: 50px" id="contact"></div>

  <div class="max-width contact-background center-horizontal">
    <div class="header-inner main-content-width center-horizontal">
      <div>
        <div class="center-horizontal" ref="contact">
          <div class="main-content-width center-horizontal">
            <div>
              <div class="center-horizontal">
                <h1 class="huge-headline center-text white">Lassen Sie uns Ihr Projekt besprechen</h1>
              </div>
              <div class="center-horizontal">
                <p class="default-textsize reset-margin center-text decent-white">Rufen Sie uns an, oder schreiben Sie eine Nachricht.</p>
              </div>
            </div>
          </div>
        </div>

        <div style="height: 50px"></div>

        <div class="center-horizontal">
          <div class="main-content-width center-horizontal contact-column">
            <div class="center-horizontal">
              <div class="address-card round-corner">
                <h2 class="reset-margin white">Kontaktinformationen</h2>
                <div style="height: 20px"></div>
                <div>
                  <div class="center-vertical">
                    <div class="full-round prim-color-background contact-circle center">
                      <Icon size="35" class="white">
                        <Call20Regular/>
                      </Icon>
                    </div>
                    <div style="width: 20px"></div>
                    <div>
                      <p class="reset-margin bold white">Adresse</p>
                      <p class="reset-margin decent-white">Musterstraße 123, 12345 Berlin</p>
                    </div>
                  </div>
                  <div style="height: 20px"></div>
                  <div class="center-vertical">
                    <div class="full-round prim-color-background contact-circle center">
                      <Icon size="35" class="white">
                        <Mail20Regular/>
                      </Icon>
                    </div>
                    <div style="width: 20px"></div>
                    <div>
                      <p class="reset-margin bold white">Telefon</p>
                      <p class="reset-margin decent-white">+49 30 12345678</p>
                    </div>
                  </div>
                  <div style="height: 20px"></div>
                  <div class="center-vertical">
                    <div class="full-round prim-color-background contact-circle center">
                      <Icon size="35" class="white">
                        <Location20Regular/>
                      </Icon>
                    </div>
                    <div style="width: 20px"></div>
                    <div>
                      <p class="reset-margin bold white">E-Mail</p>
                      <p class="reset-margin decent-white">info@bellavista-pizza.de</p>
                    </div>
                  </div>
                </div>
                <div style="height: 20px"></div>
                <div class="contact-opening round-corner">
                  <p class="bold white reset-margin">Öffnungszeiten</p>
                  <div style="height: 15px"></div>
                  <p class="decent-white reset-margin">Montag - Freitag: 7:00 - 17:00</p>
                  <div style="height: 10px"></div>
                  <p class="decent-white reset-margin">Samstag: 8:00 - 14:00</p>
                  <div style="height: 10px"></div>
                  <p class="decent-white reset-margin">Sonntag: Geschlossen</p>
                </div>
              </div>
            </div>
            <div class="contact-space"></div>
            <div class="center-horizontal">
              <div class="message-card shadow round-corner">
                <h2 class="reset-margin white">Nachricht senden</h2>
                <div style="height: 20px"></div>
                <div class="center">
                  <div class="flex-1">
                    <div>
                      <p class="reset-margin white">Vorname</p>
                    </div>
                    <div class="center-horizontal max-width">
                      <div class="input-layer">
                        <input class="input white"/>
                      </div>
                    </div>
                  </div>
                  <div class="flex-1">
                    <div>
                      <p class="reset-margin white">Nachname</p>
                    </div>
                    <div class="center-horizontal max-width">
                      <div class="input-layer">
                        <input class="input white"/>
                      </div>
                    </div>
                  </div>
                </div>
                <div style="height: 10px"></div>
                <div>
                  <p class="reset-margin white">E-Mail</p>
                </div>
                <div class="center-horizontal max-width">
                  <div class="input-layer">
                    <input class="input white">
                  </div>
                </div>
                <div style="height: 10px"></div>
                <div>
                  <p class="reset-margin white">Telefon</p>
                </div>
                <div class="center-horizontal max-width">
                  <div class="input-layer">
                    <input class="input white">
                  </div>
                </div>
                <div style="height: 10px"></div>
                <div>
                  <p class="reset-margin white">Ihr Anliegen</p>
                </div>
                <div class="center-horizontal max-width">
                  <textarea class="textarea white" style="min-height: 100px; font-size: 15px"/>
                </div>
                <div style="height: 10px"></div>
                <div class="center-horizontal">
                  <UIButton title="Absenden"/>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <Footer/>

</template>


<script>

import Nav from "@/components/views/Nav.vue"
import UIButton from "@/components/views/UIButton.vue"
import {Icon} from "@vicons/utils"
import {Shield24Regular, Star28Regular, Home24Regular, Building24Regular, Color20Regular, Clock20Regular, Call20Regular, ChevronDoubleDown20Regular, Mail20Regular, Location20Regular} from "@vicons/fluent"
import LeistungCard from "@/components/views/LeistungCard.vue";
import Footer from "@/components/views/Footer.vue"
import ProjectCard from "@/components/views/ProjectCard.vue"

export default {
  name: "MainPage",
  components: {
    ProjectCard,
    Footer, LeistungCard,
    Icon, UIButton, Nav, Shield24Regular, Star28Regular, Home24Regular, Building24Regular, Color20Regular, Clock20Regular, Call20Regular, ChevronDoubleDown20Regular, Mail20Regular, Location20Regular},
  data() {
    return {
      fadePizza: false,
      fadeHeader: false,
      fadeNav: false,
      fadeSubHeader: false,
      fadeSubButtons: false,
      fadeSubInfos: false,
    };
  },

  created() {
  },

  beforeDestroy() {
  },

  mounted() {

    setTimeout(() => {
      this.fadeNav = true
      this.fadePizza = true
      this.fadeHeader = true
    },10)

    setTimeout(() => {
      this.fadeSubHeader = true
      setTimeout(() => {
        this.fadeSubButtons = true
        setTimeout(() => {
          this.fadeSubInfos = true
        },200)
      },200)
    },500)
  },

  methods: {

    onContact(){
      const yOffset = -100;
      const element = this.$refs.contact
      const y = element.getBoundingClientRect().top + window.scrollY + yOffset;

      window.scrollTo({top: y, behavior: 'smooth'});
    },

    onProjects(){
      const yOffset = -100;
      const element = this.$refs.projects
      const y = element.getBoundingClientRect().top + window.scrollY + yOffset;

      window.scrollTo({top: y, behavior: 'smooth'});
    },

    getCookies(key) {
      return this.$cookies.get(key);
    },
    setCookies(key, value) {
      this.$cookies.set(key, value, 2147483647);
    },
  }
}
</script>