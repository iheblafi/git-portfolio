<div id="intro">
  <h1>About Me</h1>
  <p id="intro-paragraph"></p>
</div>

<script>
const introText = "Hi there! I'm [Your Name], a [Your Role/Profession] based in [Your Location]. [Add a brief description about yourself, your interests, and your expertise].";
const paragraphElement = document.getElementById("intro-paragraph");

function displayWords(text, element) {
  const words = text.split(' ');

  function displayNextWord(index) {
    if (index < words.length) {
      element.innerHTML += words[index] + ' ';
      setTimeout(() => displayNextWord(index + 1), 200); // Adjust the delay as needed
    }
  }

  displayNextWord(0);
}

displayWords(introText, paragraphElement);
</script>
