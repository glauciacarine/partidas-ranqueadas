// Função que calcula o saldo de partidas ranqueadas e determina o nível do jogador
function calcularNivel(vitorias, derrotas) {
    let saldoVitorias = vitorias - derrotas;
    let nivel;

    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 11 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else {
        nivel = "Imortal";
    }

    return { saldoVitorias, nivel };
}

// Exemplo de uso da função
let vitorias = 85;
let derrotas = 20;

let resultado = calcularNivel(vitorias, derrotas);
console.log(`O Herói tem saldo de ${resultado.saldoVitorias} está no nível de ${resultado.nivel}`);

