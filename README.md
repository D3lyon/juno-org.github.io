<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Dlinea Juno - home</title>
    <meta name="description" content="Página privada do grupo Dlinea, unidade Juno">
    <meta name="robots" content="index">
    <link href="estilo-home.css" rel="stylesheet" />
    <link href="estilo-header.css" rel="stylesheet" /> 
    <img id="object-position" src="IMG_6082.JPG" alt="imagem-terreo"

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Michroma&display=swap" rel="stylesheet">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Source+Sans+3:ital,wght@0,200..900;1,200..900&display=swap" rel="stylesheet">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
</head>
<header> <h1> D'LINEA </h1> 
<H2>JUNO</H2>
<h3>|</h3>
<div class="quadrado-header2"></div>
<div class="quadrado-header"></div>
</header>
<body>
    <script type="module">
  // Import the functions you need from the SDKs you need
  import { initializeApp } from "https://www.gstatic.com/firebasejs/11.7.3/firebase-app.js";
  import { getAnalytics } from "https://www.gstatic.com/firebasejs/11.7.3/firebase-analytics.js";
  // TODO: Add SDKs for Firebase products that you want to use
  // https://firebase.google.com/docs/web/setup#available-libraries

  // Your web app's Firebase configuration
  // For Firebase JS SDK v7.20.0 and later, measurementId is optional
  const firebaseConfig = {
    apiKey: "AIzaSyAnkmIcZfOWmdiYynMWV1FIeAoc0dlxidg",
    authDomain: "estoque-d.firebaseapp.com",
    projectId: "estoque-d",
    storageBucket: "estoque-d.firebasestorage.app",
    messagingSenderId: "4519241546",
    appId: "1:4519241546:web:428fd2832dbbe90dcac3b3",
    measurementId: "G-Y2G6WCE0SM"
  };

  // Initialize Firebase
  const app = initializeApp(firebaseConfig);
  const analytics = getAnalytics(app);
</script>
    <form id="loginForm">
    <h4><input type="email" id="Login" placeholder="Login" class="login"></h4>
    <h5><input type="password" id="Senha" placeholder="Senha" class="senha"></h5>
    <h6><button type="submit" class="botão">❯</button></h6></form>
    <p id="msg"></p>

    <script type="module">
    import { getAuth, signInWithEmailAndPassword } from "https://www.gstatic.com/firebasejs/11.7.3/firebase-auth.js";
  document.getElementById("loginForm").addEventListener("submit", function (e) {
    e.preventDefault(); // Evita o recarregamento da página

    const email = document.getElementById("Login").value;
    const password = document.getElementById("Senha").value;

    
const auth = getAuth();
signInWithEmailAndPassword(auth, email, password)
      .then((userCredential) => {
        // Sucesso no login
        const user = userCredential.user;
        window.location.href = "home.html"
    // ...
  })
  .catch((error) => {
    const errorCode = error.code;
    const errorMessage = error.message;
  });
  
  });
</script>

    <h7>Seja bem-vindo(a)!</h7>
    <h8>utilize seu nome de usuário e <br> 
        sua senha para fazer login</h8>
    
    <hr>
    <h9>Esqueceu sua senha?</h9>
    <div class="imagem-terreo"></div>
</body>
</html>
