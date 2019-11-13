

<h1> Page 3 </h1>

<h2>List of all names in random sentences</h2>

<button onclick="makeSentence()">Generate a sentence</button>

<p id="demo"></p>

<script>
function makeSentence(){
var person = {
	names: [ "Brian", "Betty", "Fiona", "Freddy", "Mini", "Marvin", "Alice", "Bob", "Jane", "Arthur", "Vincent", "Amy", "He", "She" ],
	verbs: [ "speaks", "jumps", "eats", "runs", "walks" ],
    adverbs: [ "slowly", "quickly", "nicely", "noisily"]
    };

var i;
var text = "";
for (i = 0; i < person.names.length; i++) {

name = person.names[i];
verb = person.verbs[Math.floor(Math.random() * person.verbs.length)];
adv = person.adverbs[Math.floor(Math.random() * person.adverbs.length)];

text+= name + " " + verb + " " + adv + "<br>";

document.getElementById("demo").innerHTML = text;
}

}

</script>

