# calculadora-imc
// script-imc.js

// Função para calcular o IMC
function calcularIMC(peso, altura) {
    if (altura <= 0 || peso <= 0) {
        return "Valores inválidos. Peso e altura devem ser maiores que zero.";
    }
    
    let imc = peso / (altura * altura);
    let categoria = "";
    
    if (imc < 18.5) {
        categoria = "Abaixo do peso";
    } else if (imc < 24.9) {
        categoria = "Peso normal";
    } else if (imc < 29.9) {
        categoria = "Sobrepeso";
    } else {
        categoria = "Obesidade";
    }
    
    return `IMC: ${imc.toFixed(2)} - Categoria: ${categoria}`;
}

// Exemplo de uso
console.log(calcularIMC(70, 1.75));
