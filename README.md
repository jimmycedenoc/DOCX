# DOCX
MrRio/DOCX.js 



Es una extension a la libreria MrRio/DOCX.js, basicamente lo que se aumento es poder dar un poco de estilos a lo que se escribe en el documento.

Forma de usar:

var doc = new DOCXjs();

var option = {};

doc.text('texto a escribir', options);

doc.text('It was developed by James Hall at Snapshot Media.', {});

doc.output('datauri');


el objeto option soporta:
{
  bold: bollean, 
  size: number,
  center: bollean,
  bulletPoint: {
    idGroup: number
  }
}

Especificacion de las prepiedades de las opciones:

bold: si el texto a escribir es en negrita.
size: tamaño de letra.
center: centrar texto.
bulletPoint: para agregar numeracion al texto, se necisita la propiedad idGroup para especificar los grupos de las numeraciones, el valor inicial debe ser 1


Ejemplo 


var doc = new DOCXjs();
var option = {bold: true, center: true};
doc.text('texto a escribir', options);
doc.text('It was developed by James Hall at Snapshot Media.', {bulletPoint: {idGroup: 1}});
doc.text('It was developed by James Hall at Snapshot Media.', {bulletPoint: {idGroup: 1}});
doc.text('It was developed by James Hall at Snapshot Media.', {bulletPoint: {idGroup: 1}});

doc.text('texto a escribir 2', options);
doc.text('It was developed by James Hall at Snapshot Media.', {bulletPoint: {idGroup: 2}});
doc.text('It was developed by James Hall at Snapshot Media.', {bulletPoint: {idGroup: 2}});
doc.output('datauri');
