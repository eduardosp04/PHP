PHP
===

PHP Calculadora

<html>
<head>
  <title> Calculadora </title>
</head>
<body>

    <form method="post">
    
    Valor1: <input type="text" name="valor1" size="5" />
    
    <select name="tipo">
    <option selected="selected"> Somar </option>
    <option> Subtrair </option>
    <option> Multiplicar </option>
    <option> Divir </option>
    </select>
    
    Valor2: <input type="text" name="valor2" size="5" />
    <input type="submit" name="calcular" value="calcular" />
    </form>
    
    <?php
      $valor1 = $_POST['valor1'];
      $valor2 = $_POST['valor2'];
      $tipo = $_POST['tipo'];
      
      switch($tipo){
          case="Somar": $resultado = $valor1 + $valor2; break;
          case="Subtrair": $resultado = $valor1 - $valor2; break;
          case="Multiplicar": $resultado = $valor1 * $valor2; break;
          case="Dividir": $resultado = $valor1 / $valor2; break;
      }
      
          echo("RESULTADO: ".$resultado);
    ?>
</body>
</html>
