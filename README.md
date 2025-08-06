# Estoque.html
Repo remoto do sistema de estoque da D'linea Juno

<script>
  document.getElementById("loginForm").addEventListener("submit", function (e) {
    e.preventDefault(); // Evita o recarregamento da página

    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;

    auth.signInWithEmailAndPassword(email, password)
      .then((userCredential) => {
        // Sucesso no login
        document.getElementById("msg").textContent = "Login realizado com sucesso!";
        console.log("Usuário:", userCredential.user);
        // Redirecionar ou fazer outra ação
      })
      .catch((error) => {
        // Erro no login
        document.getElementById("msg").textContent = "Erro: " + error.message;
      });
  });
</script>
