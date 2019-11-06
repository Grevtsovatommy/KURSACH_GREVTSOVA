<template>
    <div> 
        <div class="header">
        <nav class="navbar navbar-light navbar-expand-md navigation-clean-button">
            <div class="container"><a class="navbar-brand" href="#">Company Name</a><button data-toggle="collapse" class="navbar-toggler" data-target="#navcol-1"><span class="sr-only">Toggle navigation</span><span class="navbar-toggler-icon"></span></button>
                <div class="collapse navbar-collapse"
                    id="navcol-1">
                    <ul class="nav navbar-nav mr-auto">
						<div class="dropdown">
						  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownWomen" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
							Clothes
						  </button>
						  <div class="dropdown-menu" aria-labelledby="dropdownWomen" >					
							<a class="dropdown-item" href="#" @click="filter('Man')">Man</a>
							<a class="dropdown-item" href="#" @click="filter('Woman')">Woman</a>
						  </div>

						</div>
                        <div class="dropdown">
						  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMen" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
							Men
						  </button>
						  <div class="dropdown-menu" aria-labelledby="dropdownMen">
							<a class="dropdown-item" href="#">Jackets</a>
							<a class="dropdown-item" href="#">Coats</a>
							<a class="dropdown-item" href="#">Jeans</a>
						  </div>
						</div>
                        <li class="nav-item" role="presentation"><a class="nav-link" href="#">Accesories</a></li>
                        <li class="nav-item" role="presentation"><a class="nav-link" href="#">Sale</a></li>
                    </ul><span class="navbar-text actions"> <a class="login" href="#">Log In</a><a class="btn btn-light action-button" role="button" href="#">Sign Up</a></span></div>
            </div>
        </nav>
    </div>
    <div class="main">
        <div class="container">
            <div class="row">
                <!--<div class="col-md-2"></div>-->
                <div class="col-md-12">
					<h3>Women</h3>
                    <div class="row">


                        <div class="col-md-4" v-for="tovar in filtertovars" v-bind:key="tovar.id">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/coats/6457644251_1_1_4.jpg" alt=""></a>
									<!-- :src="item.photo" -->
								</div>
								<p class="product-title">
									<a href="#">{{tovar.Name}}</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										<!-- UAH 2,599.00 -->
										{{tovar.Price}}
									</p>
								</div>
							</div>
						</div>
    
                    </div>
					
					<h3>Men</h3>
					
                    <div class="row">
                        <div class="col-md-4" v-for="tovar in tovars" v-bind:key="tovar.id">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/jackets_men/6394086251_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">{{tovar.Name}}</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 1,399.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/coats_men/6406407700_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Double-sided biker jacket</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 2,199.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/jeans_men/0264211712_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Ripped jeans</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 1,399.00
									</p>
								</div>
							</div>
						</div>
                    </div>
					
					<h3>Accesories</h3>
					
                    <div class="row">
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/accesories/8880668802_4_2_1.gif" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Pompom hat</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 349.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/accesories/9234917611_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Set of pastel hair clips</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 249.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/accesories/3489588250_4_2_1.gif" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Pack of fruit print socks</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 349.00
									</p>
								</div>
							</div>
						</div>
                    </div>
					
					<h3>Sale</h3>
					
                    <div class="row">
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/sale/4222032203_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Men’s multicoloured trainers</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 1,899.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/sale/5291031202_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Contrast XL sole trainers</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 949.00
									</p>
								</div>
							</div>
						</div>
                        <div class="col-md-4">
							<div class="product">
								<div class="product-img">
									<a href="#"><img src="assets/img/sale/7232132203_1_1_4.jpg" alt=""></a>
								</div>
								<p class="product-title">
									<a href="#">Men’s multicoloured trainers</a>
								</p>
								<div class="product-buy">
									<p class="product-price">
										UAH 1,899.00
									</p>
								</div>
							</div>
						</div>
                    </div>
                </div>
            </div>
        </div>
	</div>
    </div>
</template>

<script>
    import Vue from 'vue'
	import axios from 'axios'
	import VueAxios from 'vue-axios'

    export default {
        data: function() {
            return {
				id: 0,
				name: '',
				category: '',
				tovars: clothes,
				filtertovars: []
				
            };
        },
        mounted: async function(){
			this.filtertovars = this.tovars
            // let response = await Vue.axios.get("http://46.101.212.195:3000/students");
            // console.log(response.data)
            // this.students = response.data;
            // this.$store.commit('setCount', this.students.length);
        },
        computed: {

            // getCurrentUser () {
            //     return this.$store.getters.getUser
            // } 
        },
      
        methods: {
			filter: function(cat){
				console.log(this.tovars)
				this.filtertovars = this.tovars.filter((element) => {
                    return element.Category == cat;
				});
				console.log(this.tovars)
			}
            // leave: function (el, done) {
            //     Velocity(el, { translateX: '15px', rotateZ: '50deg' }, { duration: 1500 })
            //     Velocity(el, { rotateZ: '100deg' }, { loop: 12 })
            //     Velocity(el, {
            //        rotateZ: '45deg',
            //        translateY: '30px',
            //        translateX: '30px',
            //        opacity: 0
            //     }, { complete: done })
            // },
            // useStyle: function() {
            //     this.$store.commit('setCurrentstyle', this.stl);
            // },
            // clickme: function(id) {
            //     this.students = this.students.filter((element) => {
            //         return element.id !== id;
            //     });
            // },
            // fillForm: function(id) {

            //     let foundStudent = this.students.find((element) => {
            //         return element._id == id;
            //     });
            //     this.id = foundStudent._id;
            //     this.name = foundStudent.name;
            // },
            // rplForm: function(id) {

            //     this.edit = id;
            // },
            // insert: function() {
               
            //     Vue.axios.post("http://46.101.212.195:3000/students", {
            //         name: this.name,
            //         group: this.group,
            //         isDonePr: false
            //     })
            //     .then((response) => {
            //          this.students.push({"name": this.name, "group": this.group, "_id": response.data._id});
            //         console.log(response.data)
            //     })     
            // },
            // update2: function(id) {
            //     // let foundStudent = this.students.find((element) => {
            //     //     return element._id == id;
            //     // });

            //     // Vue.axios.put("http://46.101.212.195:3000/students/"+id, {
            //     //     name: foundStudent.name,
            //     //     group: foundStudent.group,
            //     //     isDonePr: false
            //     // })
            //     // .then((response) => {
            //     //     console.log(response.data)
            //     // })    
            //     this.edit = 0; 
            // },
            // update1: function() {
            //     let foundStudent = this.students.find((element) => {
            //         return element._id == this.id;
            //     });
            //     foundStudent.name = this.name;
            //     // Vue.set(foundStudent, 'name', this.name);
                
            //     Vue.axios.put("http://46.101.212.195:3000/students/"+this.id, {
            //         name: this.name,
            //         group: this.group,
            //         isDonePr: false
            //     })
            //     .then((response) => {
            //         console.log(response.data)
            //     })    
            // },
            // deleteStudent: function(id) {
            //     Vue.axios.delete("http://46.101.212.195:3000/students/"+id)
            //     .then((response) => {
            //         this.students = this.students.filter((element) => {
            //             return element._id !== id;
            //         });
            //     this.delId = id;
            //     console.log(response.data)
            //     })     
            // }
            },
    }
</script>
<style scoped>
    .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
    opacity: 0;
    }
</style>
