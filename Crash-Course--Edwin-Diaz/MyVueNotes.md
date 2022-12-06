**Vue Notes**

**Course:** [https://www.udemy.com/course/vuejs-fast-crash-course/](https://www.udemy.com/course/vuejs-fast-crash-course/)

_ **Index Html** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

        \<divid="app"\>

            {{message}}

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

                message : "Hello"

            }

        })

    \</script\>

\</html\>

- _Directly used vue with the script src=_https://cdn.jsdelivr.net/npm/vue/dist/vue.js
- _Created a new Vue in script tag with element app and a datum message with value Hello. Then in div with tag app, displayed message in curvy brackets {{}}_

_ **String Interpolation** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

        \<divid="app"\>

            \<h2\>{{message}}\</h2\>

            \<h2\>{{number+1}}\</h2\>

            \<h2\>{{isActive?'is Active':'is Not Active'}}\</h2\>

            _\<!--if isActive == True then print is Active, else print is Not Active--\>_

            \<h2\>{{message.split('').reverse('').join('')}}\</h2\>

            _\<!--Message will be printed in reverse order._

                _Split message to letters H e l l o,_

                _Reverse order o l l e H,_

                _Join them back olleH --\>_

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

    _/\*_

        _You can change the values in Vue model, vm, through Console in Inspect of the web page._

        _To do that you can type vm.message = "Hallo" for example_

        _vm.isActive = false_

    _\*/_

        letvm=newVue({

            el: "#app",

            data: {

                message : "Hello",

                number: 10,

                isActive: false

            }

        })

    \</script\>

\</html\>

- _Created new variables, changed them through console, implemented a basic if else statement, split reverse joined a string value._

_ **Data Binding** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Data Binding\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<av-bind:href="url"\>{{url}}\</a\>

            \<h1v-bind:data="dynamicId"\>{{dynamicId}}\</h1\>

            _\<!--Use v-bind or : before binding a value from script to have it displayed.--\>_

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        letvm=newVue({

            el: "#app",

            data: {

                dynamicId:51,

                url: "https://www.github.com/3rt4nm4n"

            }

        })

    \</script\>

    \</body\>

\</html\>

- _Created a url string value, binded it to href using v-bind. For short of v-bind:href you can type :href as well._

_ **Twoway Binding** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<metacharset="UTF-8"\>

        \<metaname="viewport"content="width=device-width, initial-scale=1.0"\>

        \<metahttp-equiv="X-UA-Compatible"content="ie=edge"\>

        \<title\>Twoway Databinding\</title\>

        \<linkhref="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"rel="stylesheet"\>

    \</head\>

    \<body\>

        \<divclass="container"\>

            \<divid="app"\>

                \<formaction=""\>

                    \<divclass="col-sm-6"\>

                        \<inputv-model="message" type="text"class="form-control"\>

                    \</div\>

                \</form\>

                {{message}}

                _\<!--Whatever you type in form box the message in previous line will be the same as it's_

                    _Can be changed through console as well, like vm.message="3rt4nm4n"--\>_

            \</div\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

  ![](RackMultipart20221206-1-vr3xej_html_5ca5ef56c7614268.png)       letvm=newVue({

            el: "#app",

            data: {

  ![](RackMultipart20221206-1-vr3xej_html_e4cbb7119eef8391.png)               message : ""

            }

        })

    \</script\>

    \</body\>

\</html\>

_ **Twoway Databinding-2** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<metacharset="UTF-8"\>

        \<metaname="viewport"content="width=device-width, initial-scale=1.0"\>

        \<metahttp-equiv="X-UA-Compatible"content="ie=edge"\>

        \<title\>Twoway Databinding\</title\>

        \<linkhref="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"rel="stylesheet"\>

    \</head\>

    \<body\>

        \<divclass="container"\>

            \<divid="app"\>

                \<formaction=""\>

                    \<divclass="col-sm-6"\>

                        \<inputv-model="options" type="text"class="form-control"\>

                        _\<!--It shows the options that you checked, separated each with comma.--\>_

                    \</div\>

                \</form\>

                \<fieldsetclass="form-group"\>

                    \<legend\>Radio buttons\</legend\>

                    \<divclass="form-check"\>

                        \<labelclass="form-check-label"\>

                            \<inputv-model="options" type="checkbox"class="form-check-input"name="optionsRadios"id="optionsRadio1"value="option-1"checked\>

                            Option one

                        \</label\>

                    \</div\>

                    \<divclass="form-check"\>

                        \<labelclass="form-check-label"\>

                            \<input  v-model="options" type="checkbox"class="form-check-input"name="optionsRadios"id="optionsRadio2"value="option-2"\>

                            Option two

                        \</label\>

                    \</div\>

                    \<divclass="form-check"\>

                        \<labelclass="form-check-label"\>

                            \<input  v-model="options" type="checkbox"class="form-check-input"name="optionsRadios"id="optionsRadio3"value="option-3"\>

                            Option three is disabled

                        \</label\>

                    \</div\>

                \</fieldset\>

                \<p\> You selected {{options.join(', ')}}\</p\>

                _\<!--It shows the options that you checked, separated each with comma.--\>_

            \</div\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

  ![](RackMultipart20221206-1-vr3xej_html_64b963046e30e86d.png)       letvm=newVue({

            el: "#app",

            data: {

                options: [],

            }

        })

    \</script\>

    \</body\>

\</html\>

_ **Directives** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Directives\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<av-bind:href="url"\>{{url}}\</a\>

            \<h1v-on:click="number++"\>{{number}}\</h1\>

            \<h1 @click="number--"\>Decrease\</h1\>

            \<formaction="" @submit.prevent="number++"\>

                _\<!--@submit.prevent prevents submit button to refresh the page after clicked.--\>_

                \<buttontype="submit"\>SUBMIT\</button\>

            \</form\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

                number:10,

                url: "https://www.github.com/3rt4nm4n"

            }

        })

    \</script\>

    \</body\>

\</html\>

- _v-on:click and @click are the same._
- _Submit.prevent was used to stop refreshing the page after clicking submit button_

_ **Inline Style Binding** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Class Binding\</title\>

    \</head\>

    \<body\>

        \<style\>

            .active{

                color:green;

            }

            .notActive{

                color:red;

            }

        \</style\>

        \<divid="app"\>

            \<h1class="static" :class="{active: isActive, 'notActive': !isActive}"\>{{name}}\</h1\>

            _\<!--if isActive is true it will use active class type_

                _if isActive is false it will use notActive class type--\>_

            \<h1 :class="[isActive?'active':'notActive']"\>{{name}}\</h1\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

                isActive:false,

                name:"Onder"

            }

        })

    \</script\>

    \</body\>

\</html\>

![](RackMultipart20221206-1-vr3xej_html_c82a3c266ca9f9f9.png)

_ **Event Binding** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Inline Style Binding\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<button @click="increaseFont"\>Increase\</button\>

            \<button @click="decreaseFont"\>Decrease\</button\>

           \<div :style="{color:'red', fontSize:fontSize+'px'}"\>

            {{ message }}

           \</div\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        letvm=newVue({

            el: "#app",

            data: {

                message : "Hello",

                fontSize:12,

            },

            methods:{

                increaseFont(){

                        this.fontSize++;

                },

                decreaseFont: function(){

                        this.fontSize--;

                }

            }

        })

    \</script\>

    \</body\>

\</html\>

- _this. is used to access the values in the current Vue app._
- _When Increase is clicked fontSize will increase by 1 px,_
  - ![](RackMultipart20221206-1-vr3xej_html_dbc3d3d838b22021.png)
- _When Decrease is clicked fontSize will decrease by 1px._
  - ![](RackMultipart20221206-1-vr3xej_html_73655430aac85012.png)

_ **Conditional Rendering** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Control Structures\</title\>

        _\<!--AKA Conditional Rendering--\>_

    \</head\>

    \<body\>

        \<divid="app"\>

            \<h1v-if="isActive"\>{{name}}\</h1\>

            _\<!--if isActive is false name will not show up, if true it will be shown--\>_

            \<h1v-else-if="name==='3rt4nm4n'"\>Hello Onder\</h1\>

            _\<!--if name is 3rt4nm4n it will print Hello Onder--\>_

            \<h1v-else\>NO USER\</h1\>

            _\<!--if isActive is false and name isnt '3rt4nm4n' above line will show--\>_

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

                isActive:false,

                name : "3rt4nm4n"

            }

        })

    \</script\>

    \</body\>

\</html\>

![](RackMultipart20221206-1-vr3xej_html_46f50baae8fbae79.png)

_ **List Rendering** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Control Structures\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<ul\>

                \<liv-for="postinposts" :key="post.id"\>{{post.title}}\</li\>

            \</ul\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

  ![](RackMultipart20221206-1-vr3xej_html_57ee9f1d35f1b359.png)                posts: [

                    {id:1,title:'Post1',body:'dsnfhgrdflkgdf'},

                    {id:2,title:'Post2',body:'dsnfhgrdflkgdf'},

                    {id:3,title:'Post3',body:'dsnfhgrdflkgdf'},

                    {id:4,title:'Post4',body:'dsnfhgrdflkgdf'}

                 ]

            }

        })

    \</script\>

    \</body\>

\</html\>

- _v-for="post in posts" :key="post.id"_

_ **Computed Properties** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Index\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<h2\>{{reverseMessage}}\</h2\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        newVue({

            el: "#app",

            data: {

                message : "Hello"

            },

            computed:{

                reverseMessage(){

                    returnthis.message.split('').reverse('').join('')

                }

            }

        })

    \</script\>

    \</body\>

\</html\>

_ **Watchers** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Watchers\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<h1\>Onder Ertan {{isActive==='active'?'is Active':'is not Active'}}\</h1\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        letvm=newVue({

            el: "#app",

            data: {

                isActive: 'not active'

            },

            watch:{

                isActive: function(_newValue_){

                    console.log('Sending an email - '+_newValue_)

                }

                _//whenever isActive is 'active' this will be printed in console log.It is watching it._

            }

        })

    \</script\>

    \</body\>

\</html\>

_ **Registering Components** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Index\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<posts\>\</posts\> _\<!--Renders component posts--\>_

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        Vue.component('posts',{

            template:`\<h1\>Hello there\</h1\>`

        })

       letvm=newVue({

            el: "#app",

            data: {

                message : "Hello"

            }

        })

    \</script\>

    \</body\>

\</html\>

_ **Inline Template** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Index\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<postsinline-template\>

                \<h1 @click="display"\>HELLOss\</h1\>

            \</posts\> _\<!--whatever you put inside inline template becomes your data_

                         _when clicked on, youll get console logged--\>_

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        Vue.component('posts',{

            data(){

                return{

                }

            },

            methods: {

                display(){

                    console.log('hello')

                }

            }

        })

       letvm=newVue({

            el: "#app"

        })

    \</script\>

    \</body\>

\</html\>

    \<body\>

        \<divid="app"\>

            \<postsdata="34"\>

            \</posts\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        Vue.component('posts',{

            props:['data'],

            template: `

                  \<h1 @click="display"\>{{data}}\</h1\>

            `,

            data(){

                return{

                    message: 'Hello User'

                }

  ![](RackMultipart20221206-1-vr3xej_html_bcabd98bb268e051.png)           },

            methods: {

                display(){

                    console.log('hello')

                }

            }

        })

_ **Nesting Components** _

\<!DOCTYPEhtml\>

\<htmllang="en"\>

    \<head\>

        \<title\>Index\</title\>

    \</head\>

    \<body\>

        \<divid="app"\>

            \<posts\>\</posts\>

        \</div\>

    \<scriptsrc="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"\>\</script\>

    \<script\>

        Vue.component('posts',{

            template: `

                  \<div\>

                      \<ul\>

                        \<post v-for="post in posts" :key="post.id"\>{{post.title}}\</post\>

                      \</ul\>

                  \</div\>

            `,

            data(){

                return{

  ![](RackMultipart20221206-1-vr3xej_html_2114ecae9df917d9.png)                   posts:[

                        {id:1,title:'Post 1'},

                        {id:2,title:'Post 2'},

                        {id:3,title:'Post 3'},

                        {id:4,title:'Post 4'},

                        {id:5,title:'Post 5'},

                    ]

                }

            },

            methods: {

                display(){

                    console.log('hello')

                }

            }

        });

        Vue.component('post',{

            template:`\<li\>\<slot\>\</slot\>\</li\>`

        })

       letvm=newVue({

            el: "#app"

        })

    \</script\>

    \</body\>

\</html\>