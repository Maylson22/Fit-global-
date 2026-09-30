<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FIT GLOBAL | Academia Completa</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            fit: {
              dark: '#0F172A',
              primary: '#FF3D00',
              secondary: '#10B981',
              light: '#F8FAFC'
            }
          },
          fontFamily: { sans: ['Inter', 'system-ui', 'sans-serif'] }
        }
      }
    }
  </script>
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto { content-visibility: auto; }
      .gradient-fit { background: linear-gradient(135deg, #FF3D00 0%, #FF6D00 100%); }
    }
  </style>
</style>
</head>
<body class="bg-fit-light font-sans text-fit-dark">
  <!-- Navegação -->
  <nav class="fixed w-full z-50 bg-white/90 backdrop-blur-md shadow-sm">
    <div class="container mx-auto px-4 py-3 flex justify-between items-center">
      <a href="#" class="text-2xl font-bold text-fit-primary">FIT GLOBAL</a>
      <div class="hidden md:flex gap-8">
        <a href="#planos" class="hover:text-fit-primary transition">Planos</a>
        <a href="#sobre" class="hover:text-fit-primary transition">Sobre</a>
        <a href="#ajuda" class="hover:text-fit-primary transition">Ajuda</a>
      </div>
      <div class="flex items-center gap-3">
        <select id="idioma" class="bg-gray-100 border-0 rounded px-2 py-1 text-sm">
          <option value="pt">🇧🇷 PT</option>
          <option value="en">🇺🇸 EN</option>
          <option value="es">🇪🇸 ES</option>
        </select>
        <button id="btnAdmin" class="text-sm px-3 py-1 border rounded hover:bg-gray-100">Admin</button>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <section class="pt-32 pb-20 px-4">
    <div class="container mx-auto text-center">
      <h1 class="text-[clamp(2.5rem,6vw,4rem)] font-bold mb-6">
        Sua Academia <span class="text-fit-primary">No Mundo Todo</span>
      </h1>
      <p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto mb-10">
        Treinos personalizados, IA de atendimento, evolução completa. Pagamento único, acesso vitalício.
      </p>
      <a href="#planos" class="inline-block gradient-fit text-white font-semibold px-8 py-4 rounded-xl shadow-lg hover:shadow-xl transition transform hover:-translate-y-1">
        Ver Planos 👇
      </a>
    </div>
  </section>

  <!-- Planos -->
  <section id="planos" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-16">Escolha Seu Plano</h2>
      <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
        <!-- Individual -->
        <div class="bg-white rounded-2xl shadow-xl p-8 border-t-4 border-fit-secondary">
          <h3 class="text-2xl font-bold mb-4">Plano Individual</h3>
          <div class="mb-6">
            <div class="text-3xl font-bold">R$ 49,99</div>
            <div class="text-gray-500">$ 30 USD • € 28 EUR</div>
            <div class="text-sm text-fit-secondary mt-1">Pagamento Único • Acesso Vitalício ✅</div>
          </div>
          <ul class="space-y-3 mb-8">
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-secondary mt-1"></i> Treinos personalizados</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-secondary mt-1"></i> Acompanhamento de evolução</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-secondary mt-1"></i> IA 24h tirando dúvidas</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-secondary mt-1"></i> Acesso em todos os idiomas</li>
          </ul>
          <button class="w-full py-3 rounded-lg bg-fit-secondary text-white font-semibold hover:bg-green-600 transition">
            Comprar Individual
          </button>
        </div>

        <!-- Profissional -->
        <div class="bg-white rounded-2xl shadow-xl p-8 border-t-4 border-fit-primary relative overflow-hidden">
          <div class="absolute top-4 right-4 bg-fit-primary text-white text-xs px-3 py-1 rounded-full">MAIS COMPLETO</div>
          <h3 class="text-2xl font-bold mb-4">Academia Profissional</h3>
          <div class="mb-6">
            <div class="text-3xl font-bold">R$ 80,00</div>
            <div class="text-gray-500">$ 79,99 USD • € 69,99 EUR</div>
            <div class="text-sm text-fit-primary mt-1">Pagamento Único • Acesso Vitalício ✅</div>
          </div>
          <ul class="space-y-3 mb-8">
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-primary mt-1"></i> Tudo do Plano Individual</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-primary mt-1"></i> Gestão de alunos</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-primary mt-1"></i> Relatórios e estatísticas</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-primary mt-1"></i> Marca personalizada</li>
            <li class="flex items-start gap-2"><i class="fa fa-check text-fit-primary mt-1"></i> Suporte prioritário</li>
          </ul>
          <button class="w-full py-3 rounded-lg gradient-fit text-white font-semibold hover:opacity-90 transition">
            Comprar Profissional
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- IA Chat -->
  <section id="ajuda" class="py-20">
    <div class="container mx-auto px-4 max-w-3xl">
      <h2 class="text-2xl font-bold text-center mb-8">Assistente IA — Tire Suas Dúvidas</h2>
      <div class="bg-white rounded-xl shadow-lg p-6">
        <div id="chat-mensagens" class="h-64 overflow-y-auto mb-4 space-y-3 p-3 bg-gray-50 rounded-lg">
          <div class="bg-gray-100 p-3 rounded-lg max-w-[80%]">
            Olá! 👋 Sou a assistente da FIT GLOBAL. Como posso te ajudar hoje?
          </div>
        </div>
        <div class="flex gap-2">
          <input id="chat-input" type="text" placeholder="Digite sua dúvida..." class="flex-1 px-4 py-3 border rounded-lg">
          <button id="chat-enviar" class="px-6 py-3 bg-fit-primary text-white rounded-lg hover:opacity-90">
            Enviar
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Rodapé -->
  <footer class="bg-fit-dark text-white py-10">
    <div class="container mx-auto px-4 text-center">
      <p>FIT GLOBAL © 2026 — Todos os direitos reservados</p>
      <p class="text-sm text-gray-400 mt-2">
        <a href="#" id="link-reembolso" class="hover:underline">Política de Reembolso (7 dias)</a>
      </p>
    </div>
  </footer>

  <!-- Modal Reembolso -->
  <div id="modal-reembolso" class="fixed inset-0 bg-black/50 flex items-center justify-center z-50 hidden">
    <div class="bg-white rounded-xl p-6 max-w-md w-full mx-4">
      <h3 class="text-xl font-bold text-red-600 mb-4">⚠️ AVISO IMPORTANTE</h3>
      <p class="mb-4">Você está solicitando reembolso dentro do prazo de 7 dias.</p>
      <p class="font-semibold mb-6 text-red-600">Ao confirmar, seu acesso será ENCERRADO PERMANENTEMENTE, sem possibilidade de retorno.</p>
      <div class="flex gap-3">
        <button id="btn-cancelar-reembolso" class="flex-1 py-2 border rounded-lg hover:bg-gray-100">Cancelar</button>
        <button id="btn-confirmar-reembolso" class="flex-1 py-2 bg-red-600 text-white rounded-lg hover:bg-red-700">Confirmar Reembolso</button>
      </div>
    </div>
  </div>

  <script>
    // Idiomas
    const textos = {
      pt: { boasVindas: "Olá! 👋 Sou a assistente da FIT GLOBAL. Como posso te ajudar hoje?" },
      en: { boasVindas: "Hello! 👋 I'm the FIT GLOBAL assistant. How can I help you today?" },
      es: { boasVindas: "¡Hola! 👋 Soy la asistente de FIT GLOBAL. ¿En qué puedo ayudarte hoy?" }
    };

    // Chat IA simples
    const msgs = document.getElementById('chat-mensagens');
    const input = document.getElementById('chat-input');
    const enviar = document.getElementById('chat-enviar');

    function adicionarMensagem(texto, ehUsuario = false) {
      const div = document.createElement('div');
      div.className = `p-3 rounded-lg max-w-[80%] ${ehUsuario ? 'bg-blue-100 ml-auto' : 'bg-gray-100'}`;
      div.textContent = texto;
      msgs.appendChild(div);
      msgs.scrollTop = msgs.scrollHeight;
    }

    enviar.addEventListener('click', () => {
      const txt = input.value.trim();
      if (!txt) return;
      adicionarMensagem(txt, true);
      input.value = '';
      
      setTimeout(() => {
        adicionarMensagem("Recebi sua dúvida! Em breve terei uma resposta para você. 🤖");
      }, 800);
    });

    // Modal Reembolso
    const modal = document.getElementById('modal-reembolso');
    document.getElementById('link-reembolso').addEventListener('click', (e) => {
      e.preventDefault();
      modal.classList.remove('hidden');
    });
    document.getElementById('btn-cancelar-reembolso').addEventListener('click', () => {
      modal.classList.add('hidden');
    });
    document.getElementById('btn-confirmar-reembolso').addEventListener('click', () => {
      alert("✅ Reembolso solicitado! Acesso será encerrado.");
      modal.classList.add('hidden');
    });
  </script>
</body>
</html>
