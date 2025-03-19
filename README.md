const inputAmigos = document.getElementById("amigo");
const listaAmigos = [];
const ulListaAmigos = document.getElementById("listaAmigos");
const ulResultado = document,getElementById("resultado");
function agregarAmigo() {
    listaAmigos.push(inputAmigos.value);
    //?ulListaAmigos.innerHTML = ulListaAmigos.innerHTML + inputAmigos.value;
    ulListaAmigos.innerHTML += `<li>${inputAmigos.value}</li>`;
}

function sortearAmigo() {
    const random = Math.floor(Math.random() * listaAmigos.length);
    const amigoSecreto = listaAmigos[random];
    ulResultado.innerHTML = `<li>El amigo secreto es: ${amigoSecreto}</li>`;
}
