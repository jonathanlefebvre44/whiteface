<template>
<div class="card  ">
 
  <div class="card-body"> 
       <h1>{{ msg }}</h1>
    <h4 class="card-title">Name:{{name}}</h4>
    <p class="card-text">Age:    {{ age }}</p>
 
  <div class="hello">

    <p>
    {{ story }}
  
    </p>
    <p>
    {{ story1 }}
  
    </p>
 
  </div> </div>
</div>

<div class="alert alert-dark" role="alert">
  <a href="#" class="alert-link">An example of the the worst in the worl. But you ll
  not face this fate if your white . This programme can spit infinity an story like this.   
  Even if every date point change injustice will remain. There is still hope and you can change things.</a>. 
</div>
</template>

<script>
var age_info = 15;
var tracery = require('tracery-grammar');
 


var symbols ={ 
  'age': ['19','15','23','44','21','26'], 
  'name': ['Julius Jones','james','kerry','ina yosoun'],
 'relatives' : ['parents','girl friend','friend','mother']   ,        
  'Activities' : ['watching TV','playing videos games','playing music','taking lunch'] ,
  'Being' : ['football star','Just a kid','  being just like you','friend you ll never know'] ,
   'sentence': ['19','15','23','44','21'],          }
var dd = tracery.createGrammar(symbols);


age_info= dd.flatten('#age#')
var name_info= dd.flatten('#name#')
var relatives_info= dd.flatten('#relatives#')
var Activities_info= dd.flatten('#Activities#')
var Being_info= dd.flatten('#Being#')
var sentence_info= dd.flatten('#sentence#')

var grammar = tracery.createGrammar({
 'animal': ['panda','fox','capybara','iguana'],
'emotion': ['sad','happy','angry','jealous'],

   

  'origin1':['I am  '+name_info+', were he White Like Me.  '+name_info+' sits at home, '+Activities_info
  +'  with his  '+relatives_info+'.'+ " " 
  + ' The sound of laughter from a witty banter in the kitchen…—And then the police break in.'           ],

  'origin2':['They take him at age '+age_info+'. '+ "   "
+'He was a  '+Being_info+' , full scholarship.'

+ "   "
+'He has been on Death Row for '+sentence_info+' years.'+ "   "
+ 
'He is now in solitary confinement. '+ "   "+'He was miles away from the crime scene.'+
 "   "+'The jury was certain a black man did it.'   

],


   
});

 
grammar.addModifiers(tracery.baseEngModifiers); 

 //var result=gramar.flatten( " salut    #name#         ");


export default {
  name: 'HelloWorld',

  data() {
    return {            
      
      
      story:grammar.flatten('#origin1#'),
      story1:grammar.flatten('#origin2#'),
      age:age_info,
      name:name_info
      
      }},

  props: {
    msg: String,
   
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card{background: rgb(35, 36, 35);}
.hello{

background: rgb(35, 36, 35);
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
