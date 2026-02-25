# ARELI...
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Ti ❤️</title>

<style>
body{
    margin:0;
    padding:0;
    overflow:hidden;
    font-family: Arial, sans-serif;
    text-align:center;
    background: linear-gradient(135deg,#ff9a9e,#ff4e50);
    color:white;
}

.contenido{
    margin-top:100px;
}

button{
    background:white;
    color:#ff4e50;
    border:none;
    padding:15px 30px;
    font-size:18px;
    margin:20px;
    border-radius:30px;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.1);
}

/* Animación corazones */
@keyframes flotar{
    0%{transform:translateY(0);opacity:1;}
    100%{transform:translateY(-800px);opacity:0;}
}
</style>
</head>

<body>

<audio id="musica" loop>
    <source src="cancion.mp3" type="audio/mpeg">
</audio>

<div class="contenido">
    <h1>Hola [Areli] 💖</h1>
    <p>
        La verdad no sé cómo empezar esto porque me cuesta mucho expresarme pero la verdad quería decirte que desde que llegaste a mi vida me siento más feliz, más animado en muchos aspectos, me gusta mucho pasar tiempo contigo jugando o hablando por discord, me alegra mucho que la vida nós hiciera coincidir, en este poco tiempo que llevo de conocerte me he dado cuenta que eres una niña muy linda. Tienes una de las risas más lindas que había escuchado en mi corta vida y me gusta mucho ser el motivo por el cual ríes, eres preciosa tus ojos son los más lindos que he mirado, me gusta mucho saber que solo me ven a mi, soy muy afortunado que me diste la oportunidad de conocerte y aunque sé que aún no sé completamente todo de ti quiero seguir haciéndolo, quiero saber todo de ti hasta lo que te parezca lo más mínimo, como te lo he dicho me gustas demasiado en todos los aspectos, cada día que pasamos juntos, hablando me doy cuenta de lo mucho que estoy perdidamente enamorado de ti, és un sentimiento que aún no logro explicar pero sé que me hace sentir muy bien. Quiero seguir estando a tu lado hasta que tú me lo permitas y vivir experiencias contigo como la de algún día conocernos en persona, no sé sinceramente he pesando muchas cosas que quiero vivir contigo, quiero hacerte sentir amada y segura conmigo, asi como tu me haces sentir, puedes estar segura que mis ojos solo te ven a ti, que mi corazón solo se emociona contigo.
Y por esto mismo quiero hacerte la gran pregunta…
    </p>
    <h2>¿Puedo ser tu novio? 💕</h2>

    <button onclick="acepto()">Sí 💖</button>
    <button id="noBtn">No 🙈</button>
</div>

<script>
/* Activar música al primer clic */
document.addEventListener("click", function(){
    document.getElementById("musica").play();
});

/* Botón NO que se mueve */
const noBtn = document.getElementById("noBtn");
noBtn.addEventListener("mouseover", function(){
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.position="absolute";
    noBtn.style.left=x+"px";
    noBtn.style.top=y+"px";
});

/* Corazones flotando */
function crearCorazon(){
    const corazon=document.createElement("div");
    corazon.innerHTML="💗";
    corazon.style.position="fixed";
    corazon.style.left=Math.random()*window.innerWidth+"px";
    corazon.style.top=window.innerHeight+"px";
    corazon.style.fontSize=(Math.random()*20+20)+"px";
    corazon.style.animation="flotar 4s linear forwards";
    document.body.appendChild(corazon);

    setTimeout(()=>{corazon.remove();},4000);
}
setInterval(crearCorazon,300);

/* Cuando dice que sí */
function acepto(){
    document.body.innerHTML=`
    <div style="display:flex;flex-direction:column;justify-content:center;align-items:center;height:100vh;background:linear-gradient(135deg,#ff4e50,#ff9a9e);color:white;text-align:center;">
        <h1 style="font-size:50px;">💖 SABÍA QUE DIRÍAS QUE SÍ 💖</h1>
        <h2>Ahora oficialmente somos novios 😍</h2>
    </div>
    `;

    for(let i=0;i<120;i++){
        const corazon=document.createElement("div");
        corazon.innerHTML="💖";
        corazon.style.position="fixed";
        corazon.style.left=Math.random()*window.innerWidth+"px";
        corazon.style.top=Math.random()*window.innerHeight+"px";
        corazon.style.fontSize=(Math.random()*30+20)+"px";
        document.body.appendChild(corazon);

        setTimeout(()=>{corazon.remove();},3000);
    }
}
</script>

</body>
</html>
