| <a href="index.html">Home</a> | <a href="page2.html">Page 2</a> | <a href="page3.html">Page 3</a>

<h1>Page 4</h1>

<h2> Random Idiom Using JSON</h2>

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
