# mg-workshop-2020
Material and schedule for the genome mining workshop CIMAT 2020  
# Bioinformática  
![langebio](imagenes/langebio.png)  

En este curso aprenderás un poco de las herramientas linux, git, Google docs y microreact.  



## Calendario 10-16 Marzo 2020 

|       Domingo 10              |        Lunes 11             |      martes 12              |      Miércoles 13           |
--------------------------------|-----------------------------|-----------------------------|-----------------------------|
__B1__	PAH/LF	Introduction to secondary metabolism | __B5__	PS/LF	Gene regulation: concepts | __B9__	MGC/FBG	Tinny Earth Project initiative     | __B12__	PS/LF	Gene regulation|   
__B2__	FBG	Introduction to Genome Mining  |    __B6__	FBG/PS	Natural Products Biosynthesis     |    | __B13__	PS/LF	Genetic tools|  
__B3__ MGC/NSM [Linux bash](https://swcarpentry.github.io/shell-novice-es/),[Git](paginas/git/sesion3.md) y [markdown](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)  |__B7__	MGC/NSM	 Biosynthetic logics 1|__B10__	MGC/NSM  [AutoMLST](https://automlst.ziemertlab.com/) |__B14__	 Biosynthetic Logics 2|   
__Jueves 14__      | __Viernes 15__| __Sábado 16__       | 
__B16__	PAH	Physiology     |__B20__ B20	FBG, NSM, MGC + Maths	Future of Genome Mining| __B24__ FBG/PS	Metabolomics|  
__B17__  	FBG	Evolution     | __B21__	MGC/PS	Ecology + Interactions 1| __B25__ 	MGC/PS	Ecology + Interactions 2 |  
__B18__  [BigSCAPE](https://bigscape-corason.secondarymetabolites.org/) [AntiSMASH](https://antismash.secondarymetabolites.org/#!/start) [antiSMASHdb](https://antismash-db.secondarymetabolites.org/#!/start) |  __B22__ NS [CORASON](https://bigscape-corason.secondarymetabolites.org/) + [EvoMining](https://github.com/nselem/evomining) [Metadatos y visualización](paginas/genomica/genomica.md)| __B26__ PS/FBG GM-WS [GNPS](https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp) and MS tools   | 
  
## Informacion General  
 Dos de nuestras lecciones linux y git son parte del contenido habitual de [software carpentry](https://software-carpentry.org/) una organización dedicada a enseñar habilidades de cómuto para hacer más en menos tiempo y con menos sufrimiento, usaremos estas dos lecciones con su permiso. Las otras lecciones fueron pensadas de acuerdo a las necesidades específicas de nuestro taller.   

## Temario detallado  
<table> <tr><td> <b> B3 Linux bash </b> <br>
1.1 Linux/Unix, Principios básicos del Shell  <br>
1.2 Comandos para el manejo de archivos y directorios   <br>
1.3 Loops   <br> 
<b> 2 Git respaldo y documentación de scripts </b> <br>
2.1 La importancia de documentar y respaldar el trabajo informático <br>
2.2 Git Guardar los scripts en internet <br>
2.3 MD Crear documentación organizada <br>
2.4 Docker y la repetibilidad de resultados en maquinas <br> </td>
    <td> <b> B7  </b>  <br></td>
    <td> <b> B10 </b> <br></td>
    <td> <b> B14 </b> <br></td>
    </tr>    
  <tr>
    <td> <b>B18</b><br>
      <a href="https://bigscape-corason.secondarymetabolites.org/">Big Scape </a><br>
      <a href="https://antismash.secondarymetabolites.org/#!/start"> antiSMASH </a> <br>
      <a href="https://antismash.secondarymetabolites.org/#!/start"> antiSMASH </a> <br>
   <a href="https://mibig.secondarymetabolites.org/">MIBiG</a> <br>   </td>
    <td> <b>B22  </b><br>
      <a href="https://bigscape-corason.secondarymetabolites.org/"> CORASON </a><br>
      <a href="https://github.com/nselem/evomining"> EvoMining </a> <br>
      <a href="paginas/genomica.md"> Metadatos </a><br>
    </td>
    <td> <b>B26 </b> <br>
      <a href="https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp"> GNPS </a> <br></td>
    <td> <b> </b> </td>
    </tr> </table>    
       
____________
## Instalaciones y requerimientos previos  
<h2 id="setup">Setup</h2>  

<p>
  Para participar en este taller necesitas una computadora con linux instalado, ubuntu se recomienda para nuevos usuarios, además necesitarás acceso a un navegador como chrome o firefox. Si sueles trabajar en windows, te recomendamos git-bash, una terminal que puede servirte para manejar archivos y utilizar bash y git dentro de windows (lección 1). Sin embargo gitbash no es suficiente para la lección de EvoMining y CORASON, para estos softwares necesitas o bien una computadora con linux o bien una instalación de docker funcional en Windows.  
  </p>
<p>
  Aqui hay una referencia de posibles problemas durante la instalación.  
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Wiki de problemas de instalación y sus soluciones. </a>.
</p>

<div id="shell">  
  <h3>El Bash Shell</h3>  
  <p>  
    Bash es un intérprete de comandosque te da poder de hacer tareas simples rápidamente.  
  </p>  

  <div class="row">  
    <div class="col-md-4">  
      <h4 id="shell-windows">Windows</h4>  
      <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>  
      <ol>  
        <li>Baja para windows <a href="https://git-for-windows.github.io/">el instalador de git </a>.</li>  
        <li>Corre el instalador y sigue los siguientes pasos:  
          <ol>  
            <li>Click en "Next".</li>  
            <li>Click en "Next".</li>    
            <li>  
              <strong>  
               Manten el "Use Git from the Windows Command Prompt" seleccioinado y  click en "Next".  
              </strong>  
                Si se te olvida hacer esto algunos programas que necesitarás no funcionaran correctamente.  
                Si esto te pasa regrésate al paso anterior del instalador y selecciona la opción correcta.  
            </li>  
            <li>Click en "Next".</li>
            <li>  
              <strong>  
                Mantén "Checkout Windows-style, commit Unix-style line endings" seleccionado y click en "Next".
              </strong>
            </li>
            <li>  
              <strong>  
                Mantén "Use Windows' default console window" seleccionado y click en "Next".  
              </strong>  
            </li>  
            <li>Click en "Install".</li>
            <li>Click en "Finish".</li>  
          </ol>  
        </li>  
        <li>  
          si tu variable de ambiente "HOME" no está lista (o no sabes qué es esto):
          <ol>
            <li>Abre el prompt (Abre el menu start, escribe <code>cmd</code> y presiona enter [Enter])</li>
            <li>
              Escribe la siguiente línea en la ventana del promt exactamente como se  muestra:  
              <p><code>setx HOME "%USERPROFILE%"</code></p>  
            </li>  
            <li>Presiona [Enter], debes de ver <code>SUCCESS: Specified value was saved.</code></li>
            <li>Para salir del prompr escribe <code>exit</code> y presiona enter [Enter]</li>
          </ol>
        </li>
      </ol>
      <p>Esto te dará ambos Git y Bash en el programa Git Bash.</p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-macosx">macOS</h4>
      <p>
        El shell por default en todas las versiones de macOS es Bash, asi que no debes instalar nada.  Podrás accesar a Bash desde la Terminal
        (que se encuentra en        <code>/Applications/Utilities</code>).
        Para la instalación de Git aqui tenemos un <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
        for an example on how to open the Terminal.
        Tal vez quieras mantener la Terminal en tu dock para este taller.  
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="shell-linux">Linux</h4>
      <p>
        El shell es usualmente Bash, pero si tu máquina es diferente puedes abrir una terminal y escribir <code>bash</code>.  
        No se necesita intalar nada
      </p>
    </div>
  </div>
</div> 

