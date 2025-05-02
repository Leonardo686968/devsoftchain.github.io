<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DevSoftChain (DSC)</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }
    header {
      background-color: #1a1a1a;
      color: #fff;
      padding: 20px;
      text-align: center;
    }
    section {
      padding: 40px;
      max-width: 900px;
      margin: auto;
    }
    h2 {
      color: #1a1a1a;
    }
    .cta {
      background-color: #0057e7;
      color: white;
      padding: 15px;
      text-align: center;
      font-size: 1.2em;
      margin-top: 20px;
      border-radius: 5px;
    }
    .cta a, .cta button {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      background-color: transparent;
      border: none;
      cursor: pointer;
      font-size: 1em;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #1a1a1a;
      color: #ccc;
    }
  </style>
  <script>
    async function donate() {
      if (typeof window.ethereum !== 'undefined') {
        try {
          const accounts = await ethereum.request({ method: 'eth_requestAccounts' });
          const tx = await ethereum.request({
            method: 'eth_sendTransaction',
            params: [{
              from: accounts[0],
              to: '0xSEU_ENDERECO_ETH_AQUI', // Substitua pelo seu endereço de carteira
              value: '0x38D7EA4C68000' // 0.01 ETH em hexadecimal
            }]
          });
          alert('Doação enviada! Obrigado pelo apoio!');
        } catch (err) {
          alert('Erro ao enviar doação: ' + err.message);
        }
      } else {
        alert('MetaMask não encontrada. Instale a extensão para doar.');
      }
    }
  </script>
</head>
<body>
  <header>
    <h1>DevSoftChain (DSC)</h1>
    <p>Transformando o futuro do desenvolvimento de software com blockchain</p>
  </header>

  <section>
    <h2>O que é o DevSoftChain?</h2>
    <p>DevSoftChain é um ecossistema descentralizado que conecta desenvolvedores, empresas e usuários através de uma rede blockchain. Nosso token DSC é utilizado para pagamentos, recompensas, financiamento e governança dentro da plataforma.</p>

    <h2>Funções do Token DSC</h2>
    <ul>
      <li>Pagamento por serviços e softwares</li>
      <li>Recompensas para desenvolvedores e colaboradores</li>
      <li>Financiamento coletivo de projetos (crowdfunding)</li>
      <li>Governança descentralizada</li>
      <li>Licenciamento automatizado de software</li>
    </ul>

    <h2>Ajude a construir essa revolução!</h2>
    <p>Estamos arrecadando fundos para desenvolver e lançar o token DSC, o marketplace de software e as ferramentas que darão vida à DevSoftChain. Sua contribuição faz parte da base deste ecossistema.</p>

    <div class="cta">
      <p>Contribua com uma doação via MetaMask:</p>
      <button onclick="donate()">Doar 0.01 ETH</button>
    </div>
  </section>

  <footer>
    <p>© 2025 DevSoftChain. Todos os direitos reservados.</p>
  </footer>
</body>
</html>
