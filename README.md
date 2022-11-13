//servidor
https://pedantic-jepsen-f4a6f1.netlify.app/#/

//Para 
<para>:(int i : i ->0;[i <MN> 20]; i++) ¿:
    codigo..
:?

//Ejemplo:
<para>:(varb i => 0;i MN 10;i++){
  imprimir("luis");
}
------------------------------------------------
//while
<cycle>:([contador <MN> 20]) ¿:
    codigo...
:?

//Ejemplo:
varb contador => 0;
<cycle>:([contador MN 20]){
  imprimir("luis");
  contador++;
}
--------------------------------------------------
// do while


//Ejemplo
cost b => 9;
mientras{
  imprimir("luis");
  b--;
}<cycle>:([b DF 0]);
--------------------------------------------------
//condicional
[x <MY> y] //mayor que
[x <MN> y] //menor que
[x <DF> y] //diferente
[x <IG> y] //igual
[x <MNIG> y] //menor o gual que
[x <MYIG> y] //mayor o gual que

//Ejemplo
varb n => 7;
<si>:([n MYIG 5]){
  imprimir("luis");
  <si>:([n IG 7]){
    imprimir("orozco");
  }
}

varb n => 4;
<si>:([n MYIG 5]){
  imprimir("luis");
  <si>:([n IG 7]){
    imprimir("orozco");
  }
}sn:([n IG 4]){
  imprimir("orozco");
  <si>:([n DF 7]){
    imprimir("luis");
  }
}sn:{
  imprimir("default");
}
--------------------------------------------------
//asignación
int x : x -> 230;

//Ejemplo
varb x;
cont v => 8;
x => 3;
x => x + v;
imprimir(x);
------------------------------------------------
//declara una función
<fun>:type [NAME-> funcionPrueba](lista de paramtros...)  ¿:
    codigo...
:?

//Ejemplo
//CON TIPO
<fun>:number [Name => funcionPrueba](f # number)  {
    imprimir("luis");
    return f;
}
cost b => 9;
cost c => funcionPrueba(b);
imprimir(c);


//SIN TIPO
<fun> [Name => funcionPrueba]( f # number)  {
    imprimir("luis :" + f);
}
cost b => 10;
funcionPrueba(b);
--------------------------------------------------
//switch

//Ejemplo
cost x:number => 2;
<suiche>:(x){
  caso => [2]:
  imprimir("hola");
  break;
}








