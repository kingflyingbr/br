<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>King Flying - Agência de Viagens</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #0369a1 0%, #0ea5e9 100%);
        }
        
        .hero-pattern {
            background-image: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 20px 20px;
        }
        
        .card-shadow {
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        
        .input-focus:focus {
            box-shadow: 0 0 0 3px rgba(14, 165, 233, 0.3);
            border-color: #0ea5e9;
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Header -->
    <header class="gradient-bg text-white">
        <div class="container mx-auto px-4 py-6 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-white rounded-full flex items-center justify-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8" />
                    </svg>
                </div>
                <h1 class="text-2xl font-bold">King Flying</h1>
            </div>
            <nav>
                <ul class="flex space-x-6">
                    <li><a href="#" class="hover:text-blue-200 transition">Home</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition">Destinos</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition">Pacotes</a></li>
                    <li><a href="#" class="hover:text-blue-200 transition">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="gradient-bg hero-pattern text-white py-16">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-10 md:mb-0">
                <h2 class="text-4xl font-bold mb-4">Viaje pelo mundo com a King Flying</h2>
                <p class="text-2xl font-semibold mb-2">A MELHOR FORMA DE VOCÊ VOAR!</p>
                <p class="text-xl mb-6">Descubra os melhores destinos com pacotes exclusivos e atendimento personalizado.</p>
                <a href="#cotacao" class="bg-white text-blue-600 font-semibold px-6 py-3 rounded-lg hover:bg-blue-50 transition duration-300 inline-block">Solicite sua cotação</a>
            </div>
            <div class="md:w-1/2">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/7ef5701d-ad6b-4a48-a78a-dd3d761c103b.png" alt="Grupo feliz de turistas em frente a paisagem deslumbrante de montanhas e lago" class="rounded-lg shadow-xl" />
            </div>
        </div>
    </section>

    <!-- Cotação Section -->
    <section id="cotacao" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Solicite sua cotação de viagem</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">Preencha o formulário abaixo com os detalhes da sua viagem e nossa equipe entrará em contato com a melhor proposta para você.</p>
            </div>
            
            <div class="max-w-4xl mx-auto bg-blue-50 rounded-xl p-8 card-shadow">
                <form id="cotacaoForm" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <!-- Origem e Destino -->
                        <div>
                            <label for="origem" class="block text-sm font-medium text-gray-700 mb-1">Origem</label>
                            <input type="text" id="origem" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" placeholder="Cidade de partida" required>
                        </div>
                        <div>
                            <label for="destino" class="block text-sm font-medium text-gray-700 mb-1">Destino</label>
                            <input type="text" id="destino" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" placeholder="Cidade de destino" required>
                        </div>
                        
                        <!-- Datas -->
                        <div>
                            <label for="dataIda" class="block text-sm font-medium text-gray-700 mb-1">Data de Ida</label>
                            <input type="date" id="dataIda" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" required>
                        </div>
                        <div>
                            <label for="dataVolta" class="block text-sm font-medium text-gray-700 mb-1">Data de Volta</label>
                            <input type="date" id="dataVolta" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" required>
                        </div>
                        
                        <!-- Passageiros -->
                        <div>
                            <label for="adultos" class="block text-sm font-medium text-gray-700 mb-1">Adultos</label>
                            <select id="adultos" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus">
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                                <option value="5+">5+</option>
                            </select>
                        </div>
                        <div>
                            <label for="criancas" class="block text-sm font-medium text-gray-700 mb-1">Crianças</label>
                            <select id="criancas" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus">
                                <option value="0">0</option>
                                <option value="1">1</option>
                                <option value="2">2</option>
                                <option value="3">3</option>
                                <option value="4">4</option>
                            </select>
                        </div>
                        
                        <!-- Classe e Hospedagem -->
                        <div>
                            <label for="classe" class="block text-sm font-medium text-gray-700 mb-1">Classe da Viagem</label>
                            <select id="classe" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus">
                                <option value="economica">Econômica</option>
                                <option value="executiva">Executiva</option>
                                <option value="primeira">Primeira Classe</option>
                            </select>
                        </div>
                        <div>
                            <label for="hospedagem" class="block text-sm font-medium text-gray-700 mb-1">Tipo de Hospedagem</label>
                            <select id="hospedagem" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus">
                                <option value="hotel">Hotel</option>
                                <option value="resort">Resort</option>
                                <option value="apartamento">Apartamento</option>
                                <option value="hostel">Hostel</option>
                            </select>
                        </div>
                        
                        <!-- Transporte -->
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Meios de Transporte</label>
                            <div class="space-y-2">
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus" checked>
                                    <span class="ml-2 text-gray-700">Avião</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Ônibus</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Trem</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Cruzeiro</span>
                                </label>
                            </div>
                        </div>
                        
                        <!-- Serviços Extras -->
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Serviços Extras</label>
                            <div class="space-y-2">
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Seguro Viagem</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Aluguel de Carro</span>
                                </label>
                                <label class="flex items-center">
                                    <input type="checkbox" class="rounded text-blue-600 input-focus">
                                    <span class="ml-2 text-gray-700">Guia Turístico</span>
                                </label>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Informações de Contato -->
                    <div class="pt-4 border-t border-gray-200">
                        <h3 class="text-lg font-medium text-gray-800 mb-4">Informações de Contato</h3>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="nome" class="block text-sm font-medium text-gray-700 mb-1">Nome Completo</label>
                                <input type="text" id="nome" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" required>
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">E-mail</label>
                                <input type="email" id="email" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" required>
                            </div>
                            <div>
                                <label for="telefone" class="block text-sm font-medium text-gray-700 mb-1">Telefone</label>
                                <input type="tel" id="telefone" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" required>
                            </div>
                            <div>
                                <label for="melhorHorario" class="block text-sm font-medium text-gray-700 mb-1">Melhor Horário para Contato</label>
                                <select id="melhorHorario" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus">
                                    <option value="manha">Manhã (8h-12h)</option>
                                    <option value="tarde">Tarde (13h-18h)</option>
                                    <option value="noite">Noite (18h-21h)</option>
                                </select>
                            </div>
                        </div>
                        <div class="mt-4">
                            <label for="observacoes" class="block text-sm font-medium text-gray-700 mb-1">Observações Adicionais</label>
                            <textarea id="observacoes" rows="3" class="w-full px-4 py-2 rounded-lg border border-gray-300 input-focus" placeholder="Alguma informação adicional sobre sua viagem?"></textarea>
                        </div>
                    </div>
                    
                    <div class="flex justify-end">
                        <button type="submit" class="gradient-bg text-white font-semibold px-6 py-3 rounded-lg hover:opacity-90 transition duration-300">
                            Solicitar Cotação
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </section>

    <!-- Depoimentos -->
    <section class="py-16 bg-blue-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">O que nossos clientes dizem</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 rounded-xl card-shadow">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                            <span class="text-blue-600 font-bold">A</span>
                        </div>
                        <div class="ml-4">
                            <h4 class="font-semibold text-gray-800">Ana Silva</h4>
                            <div class="flex text-yellow-400">
                                <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">"A King Flying tornou minha viagem para a Europa incrível. O atendimento foi personalizado e superaram todas as minhas expectativas!"</p>
                </div>
                
                <div class="bg-white p-6 rounded-xl card-shadow">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                            <span class="text-blue-600 font-bold">C</span>
                        </div>
                        <div class="ml-4">
                            <h4 class="font-semibold text-gray-800">Carlos Mendes</h4>
                            <div class="flex text-yellow-400">
                                <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">"Excelente agência!Sem vocês não seria possível eu viver o que vivi em Malta, obrigado por essa experiência inesquecível."</p>
                </div>
                
                <div class="bg-white p-6 rounded-xl card-shadow">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
                            <span class="text-blue-600 font-bold">J</span>
                        </div>
                        <div class="ml-4">
                            <h4 class="font-semibold text-gray-800">Juliana Alves</h4>
                            <div class="flex text-yellow-400">
                                <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
                            </div>
                        </div>
                    </div>
                    <p class="text-gray-600">"Recomendo a King Flying para todos que querem planejar uma viagem perfeita sem preocupações. O suporte 24h fez toda diferença!"</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="gradient-bg text-white py-16">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold mb-6">Pronto para sua próxima aventura?</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">Nossa equipe está pronta para te ajudar a planejar a viagem dos seus sonhos.</p>
            <a href="#cotacao" class="bg-white text-blue-600 font-semibold px-8 py-3 rounded-lg hover:bg-blue-50 transition duration-300 inline-block">Solicite sua cotação agora</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-blue-900 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-lg font-semibold mb-4">King Flying</h3>
                    <p class="text-blue-200">Sua agência de viagens confiável, oferecendo os melhores serviços e destinos com qualidade e segurança.</p>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">Links Úteis</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-blue-200 hover:text-white transition">Pacotes Promocionais</a></li>
                        <li><a href="#" class="text-blue-200 hover:text-white transition">Destinos Populares</a></li>
                        <li><a href="#" class="text-blue-200 hover:text-white transition">Dicas de Viagem</a></li>
                        <li><a href="#" class="text-blue-200 hover:text-white transition">Termos e Condições</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">Contato</h4>
                    <ul class="space-y-2 text-blue-200">
                        <li class="flex items-start">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mt-0.5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                            </svg>
                            +351 932 091 853
                        </li>
                        <li class="flex items-start">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mt-0.5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                            </svg>
                            kingflyingbr@gmail.com
                        </li>
                        <li class="flex items-start">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mt-0.5 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                            </svg>
                            Rua Santos Anjos, 295 - Belo Horizonte/MG
                        </li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4">Redes Sociais</h4>
                    <div class="flex space-x-4">
                        <a href="https://instagram.com/kingflyingbr" target="_blank" class="bg-blue-800 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-700 transition">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z" />
                            </svg>
                        </a>
                        <a href="#" class="bg-blue-800 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-700 transition">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-.796c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 2.163c-3.115 0-5.653 2.538-5.653 5.652s2.538 5.653 5.653 5.653 5.653-2.539 5.653-5.653-2.538-5.652-5.653-5.652zm0 9.416c-2.076 0-3.764-1.689-3.764-3.764s1.688-3.764 3.764-3.764 3.764 1.688 3.764 3.764-1.689 3.764-3.764 3.764zm5.323-6.667c-.737 0-1.334-.597-1.334-1.334s.597-1.334 1.334-1.334 1.334.597 1.334 1.334-.597 1.334-1.334 1.334z" />
                            </svg>
                        </a>
                        <a href="#" class="bg-blue-800 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-700 transition">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24">
                                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
            <div class="border-t border-blue-800 mt-8 pt-8 text-center text-blue-300">
                <p>© 2024 King Flying. Todos os direitos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('cotacaoForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Simulando envio do formulário
            const nome = document.getElementById('nome').value;
            
            // Exibindo mensagem de sucesso
            alert(`Obrigado, ${nome}! Sua cotação foi recebida com sucesso. A equipe King Flying entrará em contato em breve.`);
            
            // Resetar formulário (opcional)
            this.reset();
        });
        
        // Ajustar data mínima para evitar datas passadas
        const hoje = new Date();
        const amanha = new Date(hoje);
        amanha.setDate(amanha.getDate() + 1);
        
        const dataIdaInput = document.getElementById('dataIda');
        const dataVoltaInput = document.getElementById('dataVolta');
        
        const formatDate = (date) => {
            return date.toISOString().split('T')[0];
        };
        
        dataIdaInput.min = formatDate(amanha);
        dataIdaInput.addEventListener('change', function() {
            const dataIda = new Date(this.value);
            const minVolta = new Date(dataIda);
            minVolta.setDate(minVolta.getDate() + 1);
            dataVoltaInput.min = formatDate(minVolta);
            
            if (new Date(dataVoltaInput.value) < minVolta) {
                dataVoltaInput.value = formatDate(minVolta);
            }
        });
    </script>
</body>
</html>


