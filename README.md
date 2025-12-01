[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21902276&assignment_repo_type=AssignmentRepo)
# 🧩 Atividade 01 – Fundamentos de Programação Estruturada (JavaScript)

Este repositório contém exercícios introdutórios de lógica e algoritmos em JavaScript, pensados para quem está começando a programar. O foco é praticar:
- escrita de funções,
- uso de condicionais (if / ternário),
- operações aritméticas básicas,
- e leitura/execução de testes automatizados.

## Objetivos de aprendizagem
- Entender como receber parâmetros numa função e retornar valores.
- Usar condicionais para tomar decisões.
- Calcular e interpretar médias e comparações.
- Executar testes automatizados com Jest para validar seu código.

---

## Estrutura do repositório

- src/: arquivos que devem ser completados com as soluções dos exercícios.
  - src/exercicio1.js — função somar(a, b)
  - src/exercicio2.js — função verificarIdade(i)
  - src/exercicio3.js — função media(a, b, c)
- tests/: testes automatizados em Jest que validam as implementações.
- package.json: configura o comando de teste (`npm test`).

---

## Pré-requisitos

- Node.js (v14+ recomendado)
- npm (v6+)

Se não tiver o Node instalado, instale-o a partir de https://nodejs.org/

---

## Como executar os testes (passo a passo)

1. Clone o repositório (se ainda não o fez):

   ```bash
   git clone https://github.com/GUIPETAV/UC3-Aula-1-Logica-e-algoritmos.git
   cd UC3-Aula-1-Logica-e-algoritmos
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Execute os testes:

   ```bash
   npm test
   ```

Os testes usarão o Jest para verificar se as funções em src/ retornam os valores esperados. Leia as mensagens do Jest — elas indicam quais casos falharam e por quê.

**Dica rápida:** enquanto desenvolve, você pode rodar apenas um teste com:
- `npm test -- -t "nome do teste"` (dependendo de como os testes foram escritos)

---

## Descrição detalhada dos exercícios (com exemplos e dicas)

### 1) src/exercicio1.js — somar(a, b)
- **Objetivo:** retornar a soma dos dois números recebidos como parâmetros.
- **Comportamento esperado:**
  - se chamarmos `somar(2, 3)` deve retornar `5`
  - se chamarmos `somar(-1, 1)` deve retornar `0`
- **Dica:** assegure-se de retornar um número (não string). Não concatene valores como string.
- **Exemplo de implementação** (apenas referência):

```javascript
function somar(a, b) {
  return a + b;
}
```

- **Casos para testar mentalmente:**
  - números inteiros positivos e negativos
  - zero
  - valores decimais

---

### 2) src/exercicio2.js — verificarIdade(i)
- **Objetivo:** receber um número representando idade e retornar:
  - "maior" se a idade for maior ou igual a 18
  - "menor" se a idade for menor que 18
- **Exemplo:**
  - `verificarIdade(18)` → "maior"
  - `verificarIdade(17)` → "menor"
- **Dicas:**
  - use `>=` para incluir exatamente 18 como "maior"
  - certifique-se de retornar strings exatamente como "maior" ou "menor" (aspas indicam string)
- **Exemplo de implementação** (apenas referência):

```javascript
function verificarIdade(i) {
  return i >= 18 ? "maior" : "menor";
}
```

- **Observação:** os testes normalmente assumem que `i` é um número; se quiser tornar a função mais robusta, pode validar o tipo, mas só faça isso se souber que os testes aceitam.

---

### 3) src/exercicio3.js — media(a, b, c)
- **Objetivo:** calcular a média aritmética dos três números e retornar:
  - "aprovado" se a média for maior ou igual a 7
  - "reprovado" caso contrário
- **Fórmula da média:** `(a + b + c) / 3`
- **Exemplo:**
  - `media(7, 7, 7)` → "aprovado"
  - `media(6, 7, 7)` → "reprovado" (média = 6.666...)
- **Dicas:**
  - lembre-se de parênteses para garantir a operação correta
  - compare a média com 7 usando `>=`
- **Exemplo de implementação** (apenas referência):

```javascript
function media(a, b, c) {
  const m = (a + b + c) / 3;
  return m >= 7 ? "aprovado" : "reprovado";
}
```

- **Atenção aos casos de ponto flutuante:** 6.999... deve ser tratado conforme os testes esperam (use `>= 7`).

---

## Boas práticas recomendadas (para este exercício)
- Mantenha funções pequenas e com responsabilidade única.
- Use nomes de variáveis descritivos (por exemplo, `mediaDoAluno`).
- Evite mutações desnecessárias.
- Comente apenas trechos de lógica que não são triviais.
- Execute os testes frequentemente enquanto desenvolve para identificar regressões cedo.

---

## Dicas de depuração rápida
- Imprima valores com `console.log()` ao rodar testes localmente (remova depois).
- Rode um único teste com Jest para focar em uma função.
- Se um teste falhar, leia a mensagem do Jest e verifique o valor esperado vs. recebido.

---

## Como contribuir
Contribuições são bem-vindas. Fluxo sugerido:
1. Fork do repositório.
2. Crie uma branch com um nome descritivo (ex.: `feat/exercicio2-fix`).
3. Faça commits claros e pequenos.
4. Abra um Pull Request descrevendo as alterações e os motivos.
5. Aguarde revisão e faça ajustes conforme feedback.

---

## Ideias para estender os exercícios (opcional)
- Validar tipos de entrada e retornar mensagens de erro amigáveis.
- Criar uma versão que leia entradas do terminal (`process.argv`).
- Escrever testes adicionais cobrindo casos extremos.

---

## Licença
Projeto disponível sob licença MIT.

---

Boa prática e bons estudos!