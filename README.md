function tocaSomPom(id.ElementoAudio){
 const elemento= document.querySelector(SeletorAudio);
 
 alert('elemento não encontrado')
 if (elemento && elemento.localName==='audio'){
 elemento.play();
 }
 else{
 alert('elemento não encontrado ou seletor inválido');
}
const listadeTeclas=document.querySelectotAll('.tecla');

let contador = 0;

for (let contador = 0; contador < listaDeTeclas.length; contador++) {
 
  const tecla= listadeTeclas[contador];
  const instrumento= tecla.classlist[1];
  const idAudio=`#som_$(instrumento)´;

    tecla.onclick=function(){
    tocaSom(idAudio);
}
contador=contador+1;

tecla.onkeydown=function(){
if(evento.code==='Enter'||evento.code==='Space'){
tecla.classlist.add('ativa')
}
tecla.onkeyup=function(){
tecla.classlist.remove('ativa')
}
}
