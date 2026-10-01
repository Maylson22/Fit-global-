<li class="flex items-start gap-2"><i class="fa fa-check text-fit-secondary mt-1"></i> Acesso em todos os idiomas</li>
          </ul>
          <button class="w-full py-3 rounded-lg bg-fit-secondary text-white font-semibold hover:bg-green-600 transition">
            Comprar Individual
          </button>
        </div>

        <!-- Academia Profissional -->
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

  <!-- Assistente IA -->
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

  <!-- Rodapé com Política de Reembolso -->
  <footer class="bg-fit-dark text-white py-10">
    <div class="container mx-auto px-4 text-center">
      <p>FIT GLOBAL © 2026 — Todos os direitos reservados</p>
      <p class="text-sm text-gray-400 mt-2">
        <a href="#" id="link-reembolso" class="hover:underline">Política de Reembolso (7 dias)</a>
      </p>
    </div>
  </footer>

  <!-- Modal de Reembolso com aviso de BLOQUEIO PERMANENTE -->
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
    // Chat da IA
    const msgs = document.getElementById('chat-mensagens');
    const input = document.getElementById('chat-input');
    const enviar = document.getElementById('chat-enviar');

    function adicionarMensagem(texto, ehUsuario = false) {
      const div = document.createElement('div');
      div.className = p-3 rounded-lg max-w-[80%] ${ehUsuario ? 'bg-blue-100 ml-auto' : 'bg-gray-100'};
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
        adicionarMensagem("Recebi sua dúvida! Estou processando... 🤖");
      }, 600);
    });

    // Modal de Reembolso
    const modal = document.getElementById('modal-reembolso');
    document.getElementById('link-reembolso').addEventListener('click', (e) => {
      e.preventDefault();
      modal.classList.remove('hidden');
    });
    
    document.getElementById('btn-cancelar-reembolso').addEventListener('click', () => {
      modal.classList.add('hidden');
    });
    
    document.getElementById('btn-confirmar-reembolso').addEventListener('click', () => {
      alert("✅ Reembolso solicitado! Seu acesso foi encerrado permanentemente.");
      modal.classList.add('hidden');
    });
  </script>
</body>
</html>
