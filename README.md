<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Gerador de Scripts Blocks Fruits</title>
<style>
  body { font-family: Arial, sans-serif; padding: 20px; background: #121212; color: #eee; }
  h1 { color: #1DB954; }
  textarea { width: 100%; height: 120px; font-size: 16px; padding: 10px; border-radius: 8px; border: none; }
  button { margin-top: 10px; padding: 15px; background: #1DB954; border: none; color: white; font-size: 18px; cursor: pointer; border-radius: 8px; }
  pre { background: #222; padding: 15px; border-radius: 8px; margin-top: 15px; white-space: pre-wrap; }
</style>
</head>
<body>
  <h1>Gerador de Scripts para Blocks Fruits</h1>
  <textarea id="inputText" 
placeholder="Descreva o script que deseja..."></textarea>
  <button id="generateBtn">Gerar Script</button>
  <pre id="outputScript"></pre>

<script>
  const generateBtn = document.getElementById("generateBtn");
  const inputText = document.getElementById("inputText");
  const outputScript = document.getElementById("outputScript");

  generateBtn.onclick = async () => {
    const prompt = inputText.value.trim();
    if(!prompt) {
      alert("Por favor, escreva o que deseja no script.");
      return;
    }
    outputScript.textContent = "Gerando script... aguarde.";

    // Aqui você colocaria a chamada à API da OpenAI
    // Exemplo de fetch para backend que chama a IA:
    /*
    const response = await fetch('/api/generate-script', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ prompt })
    });
    const data = await response.json();
    outputScript.textContent = data.script || "Erro ao gerar script.";
    */

    // Como exemplo, só vamos simular a resposta:
    setTimeout(() => {
      outputScript.textContent = `-- Script gerado para: ${prompt}\nprint("Script pronto para você!")`;
    }, 1500);
  };
</script></html>
