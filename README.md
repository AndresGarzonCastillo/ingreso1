# ingreso1
nodejs
const edad = parseInt(prompt("¿Cuál es tu edad?"));
const promesaIngreso = new Promise ((resolve, reject) => {
  if (edad >= 18) {
    resolve ("Eres mayor de edad, puedes ingresar");
} else if (edad <= 17){
    reject ("Eres menor de edad, no puedes ingresar");
  }
  else {
    reject ("El documento presentado no es valido");
}
});
promesaIngreso.then((valor) => {
  console.log(`started ${valor}`);
}).catch((error)=>{
  console.log(error);
});
