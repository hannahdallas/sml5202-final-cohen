<a href="page2.html">Page 2</a> | <a href="page3.html">Page 3</a>
<h1>1. Section 1 </h1>

<p> 
  
 Hi! My name is Hannah Cohen, I am 21 years old, and I am from Westchester, New York. I am in my third year of university studying Economics at Northwestern in Chicago but am studying abroad for the semester at Queen Mary in London.

<a href="https://hub.qmplus.qmul.ac.uk/view/view.php?profile=hannah-rivka-cohen&page=sml5202-hannah-s-page"> Visit my QMplus Hub page </a>

</p> 

<hr>

<h1> 2. Section 2 </h1>

<p> Things I have to do </p>
  <ul>
  <li> Apply to internships </li>
  <li> Plan trip to Nice </li>
  <li> Call my grandpa </li>
  </ul>

<hr>

<h1> 3. Section 3 </h1>

<p> My favorite things </p>
  <ol>
  <li> Speed boats </li>
  <li> Fireworks </li>
  <li> Flowers </li>
  </ol>
  
  <hr>

<h1> Random Idiom Using JSON</h1>

<button type="button" class="new-quote button">Show Idiom</button>
<dl id="quote"></dl>

<script>
const endpoint = 'https://hannahrcohen.github.io/sml5202-cohen/datasets/idioms.json';

function getQuote() {
fetch(endpoint)
.then(function (response) {
return response.json();
})
.then(function(data){
let id = Math.floor(Math.random() * 6);
let idiom = (data.idioms[id].idiom);
let meaning = (data.idioms[id].meaning);
let example = (data.idioms[id].example);

document.querySelector("#quote").innerHTML = "<dt>" + idiom + "</dt>" + "<dd><strong>Example:</strong> " + example + "</dd><dd><strong>Meaning:</strong>" + meaning + "</dd>";

//console.log(data.idioms[id].idiom)
})

.catch(function () {
console.log("Error occurred");
});
}

const newQuoteButton = document.querySelector('.new-quote');
newQuoteButton.addEventListener('click', getQuote);

</script>
