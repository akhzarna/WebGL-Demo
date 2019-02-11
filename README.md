# WebGL-Demo
Simple Code to start WebGL is given Below


<html>
  <head>
    <title> WebGL testing </title>
    
      <script language = "javascript">

      function initialiseWebGL(){

      var canvas = document.getElementById("gl");

      var gl =  canvas.getContext("webgl") ||
                canvas.getContext("experimental-webgl") ||
                canvas.getContext("moz-webgl") ||
                canvas.getContext("webkit-3d");

      if (gl) {
        var extensions = gl.getSupportedExtensions();
        console.log("Gl is working");
        console.log(gl);
        console.log(extensions);

        gl.viewportWidth = canvas.width;
        gl.viewportHeight = canvas.height;
        gl.clearColor(0.0,0.0,0.0,1.0);
        gl.clear(gl.COLOR_BUFFER_BIT);

      }else{
        console.log("gl is not initialised");
      }
}
</script>


</head>

  <body onload = "initialiseWebGL()">

    <h1>
      TESTING WebGL
    </h1>

    <canvas id = "gl" width = "400" height = "500">
    </canvas>

  </body>
</html>
