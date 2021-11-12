---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Nous contacter
order: 1
---

<form id="my-form" action="https://formspree.io/f/mayarqel" method="POST">
  <label>
    Votre adresse de messagerie:<br/>
    <input size=30 type="email" name="_replyto">
  </label><br/>
  <label>
    Votre message:<br/>
    <textarea cols=30 rows=10 name="text"></textarea><br/>
  </label>
  <!-- your other form fields go here -->
  <button type="submit">Nous contacter</button>
  <p id="my-form-status"></p>
</form>

<script>
    var form = document.getElementById("my-form");
    
    async function handleSubmit(event) {
      event.preventDefault();
      var status = document.getElementById("my-form-status");
      var data = new FormData(event.target);
      fetch(event.target.action, {
        method: form.method,
        body: data,
        headers: {
            'Accept': 'application/json'
        }
      }).then(response => {
        status.innerHTML = "Merci pour votre message, nous vous répondrons rapidement !";
        form.reset()
      }).catch(error => {
        status.innerHTML = "Zut, on dirait que cela n'a pas fonctionné, reessayez plus tard !"
      });
    }
    form.addEventListener("submit", handleSubmit)
</script>
