<template>
    <main class="container">
        <div class="row">
            <div class="col-12">
                <h1 class="text-center color-FFAB4D fw-bolder">Our latest work performed</h1>
            </div>
            <div v-for="[i, project] in projects.entries()" class="row mt-4 mb-4">
                <div :class="`${i%2 == 0 ? 'description col-12 col-md-6 col-lg-6 d-grid align-items-center' : actualSize <= 767 ? 'description col-12 col-md-6 col-lg-6 d-grid align-items-center' : 'description col-12 col-md-6 col-lg-6 d-grid align-items-center order-2'}`">
                    <div class="section">
                        <h3 class="text-center color-FFAB4D img-title">{{ project.title }}</h3>
                        <p class="text-center">{{ project.description }}</p>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-6">
                    <img v-motion-pop v-motion-pop-visible :src="project.imgPath" class="img border border-warning rounded-5 shadow-FFAB4D" loading="lazy">
                </div>
            </div>
        </div>
    </main>
</template>
<script>
export default {
    data() {
        return {
            projects: [
                {
                    title: 'Matte CG',
                    description: 'Recognized Ecuadorian Animation Studio, VFX and Film, with a long history in the creation of custom projects fo content and advertising workdwide.',
                    imgPath: '/src/assets/matte.svg'
                },
                {
                    title: 'Rahua',
                    description: 'It was developed for a large and recognized ecommerce company that is dedicated to the care of hair, skin and face, with natural and pure organic ingredients derived from plants.',
                    imgPath: '/src/assets/rahua.svg'
                },
                {
                    title: 'De Chez Moi',
                    description: 'Entrepreneurship by Juan Pablo Aguilar Lliguin, De Chez Moí is an ecommerce dedicated to the development of high-end organic chocolates.',
                    imgPath: '/src/assets/dechezmoi.svg'
                },
                {
                    title: 'EPS S.A',
                    description: 'Electric Power Solutions, Company focused on the electricity sector, with a big experience in the commercialization of equipment and supplies for electrical distribution, transmission and substation systems.',
                    imgPath: '/src/assets/eps.svg'
                },
                {
                    title: 'Club Mécanique Des Femmes',
                    description: 'It is an idea created by Annie Barrette, whose main objective is to offer basic car maintenance workshops for women, throughout Quebec.',
                    imgPath: '/src/assets/club-mecanique.svg'
                },
                {
                    title: 'Tour en Praga',
                    description: 'Tour in Prague, is a company dedicated to offer different tours and excursions in Spanish in the city of Prague, Czech Republic.',
                    imgPath: '/src/assets/tourenpraga.svg'
                },
            ],
            actualSize: window.innerWidth,
        }
    },
    created() {
        window.addEventListener("resize", this.orderContent);
    },
    destroyed() {
        window.removeEventListener("resize", this.orderContent);
    },
    methods: {
        orderContent() {
            const actualSize = window.innerWidth;
            if(actualSize <= 767) {
                document.querySelectorAll('.order-2').forEach(element => {
                    element.classList.remove('order-2')
                })
                return
            }
            document.querySelectorAll('.description').forEach((element, i) => {
                if(element.classList.contains('order-2')) {}
                else {
                    if(i%2 != 0) {
                        element.classList.add('order-2')
                    }
                }
            })
        }
    },
    mounted() {
        console.log(window.innerWidth)
        document.title = "CacaoWebStudio - Projects"
    }
}
</script>
<style>
    .color-FFAB4D {
        color: #FFAB4D;
    }
    .shadow-FFAB4D {
        box-shadow: 1px 1px 5px #FFAB4D;
    }
    .img-title:hover {
        text-shadow: 0px 0px 2px #FFAB4D;
        cursor: pointer;
    }
</style>