# nicollasantos.com.br
testes html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Sono Primordial - Descubra seu Perfil de Sono</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #1a237e 0%, #283593 100%);
            color: #fff;
            min-height: 100vh;
        }
        .quiz-container {
            max-width: 800px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.1);
            overflow: hidden;
 .question {
            display: none;
        }
        .question.active {
            display: block;
            animation: fadeIn 0.5s ease-in-out;
        }
        .option-btn {
            background-color: rgba(255, 255, 255, 0.15);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }
        .option-btn:hover {
            background-color: rgba(255, 255, 255, 0.25);
            transform: translateY(-2px);
        }
        .option-btn.selected {
            background-color: #5C6BC0;
            border-color: #3F51B5;
        }
        .progress-bar {
            height: 8px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            overflow: hidden;
        }
        .progress {
            height: 100%;
            background-color: #7986CB;
            border-radius: 4px;
            transition: width 0.3s ease;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .sleep-icon {
            width: 32px;
            height: 32px;
        }
        .moon-icon {
            filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.7));
        }
        input::placeholder {
            color: rgba(255, 255, 255, 0.5);
        }
    </style>
</head>
<body class="p-4 md:p-8">
    <div class="quiz-container p-6 md:p-10 my-8">
        <header class="mb-8 text-center">
            <div class="flex justify-center items-center mb-4">
                <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/svg/1f4a4.svg" alt="Sono" class="sleep-icon mr-2">
                <h1 class="text-3xl md:text-4xl font-bold text-white">Sono Primordial</h1>
                <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/svg/1f319.svg" alt="Lua" class="sleep-icon ml-2 moon-icon">
            </div>
            <p class="text-lg md:text-xl text-blue-100">Descubra seu perfil de sono e receba um plano personalizado para noites mais tranquilas e dias mais produtivos.</p>
            <p class="text-sm md:text-base text-blue-200 mt-2">Este quiz leva apenas 3 minutos e pode transformar seus próximos 30 anos de sono!</p>
            
            <div class="progress-bar mt-6">
                <div class="progress" id="progress-bar" style="width: 0%"></div>
            </div>
            <p class="text-sm mt-2"><span id="current-question">1</span>/19</p>
        </header>

        <div id="quiz-content">
            <!-- Pergunta 1 -->
            <div class="question active" data-question="1">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">1. Qual o seu gênero?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="feminino">
                        <span class="mr-3 text-xl">🔘</span> Feminino
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="masculino">
                        <span class="mr-3 text-xl">🔘</span> Masculino
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="outro">
                        <span class="mr-3 text-xl">🔘</span> Prefiro não dizer
                    </button>
                </div>
                <p class="text-sm text-blue-200 mt-4 italic">(Pergunta fácil e obrigatória para segmentação.)</p>
            </div>

            <!-- Pergunta 2 -->
            <div class="question" data-question="2">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">2. Qual a sua faixa etária?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="menos20">
                        <span class="mr-3 text-xl">🔘</span> Menos de 20 anos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="20a30">
                        <span class="mr-3 text-xl">🔘</span> Entre 20 e 30 anos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="31a40">
                        <span class="mr-3 text-xl">🔘</span> Entre 31 e 40 anos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="41a50">
                        <span class="mr-3 text-xl">🔘</span> Entre 41 e 50 anos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="mais50">
                        <span class="mr-3 text-xl">🔘</span> Mais de 50 anos
                    </button>
                </div>
                <p class="text-sm text-blue-200 mt-4 italic">(Outra simples, mas essencial para personalizar o resultado.)</p>
            </div>

            <!-- Pergunta 3 -->
            <div class="question" data-question="3">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">3. Você gostaria de aprender a dormir do jeito certo — e acordar renovado(a) todos os dias?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sim">
                        <span class="mr-3 text-xl">🔘</span> Sim, com certeza
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="talvez">
                        <span class="mr-3 text-xl">🔘</span> Talvez
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="naotenho">
                        <span class="mr-3 text-xl">🔘</span> Não tenho certeza
                    </button>
                </div>
                <p class="text-sm text-blue-200 mt-4 italic">(Persuasiva, com foco no desejo. Já começa a guiar o pensamento da pessoa pro benefício.)</p>
            </div>

            <!-- Pergunta 4 -->
            <div class="question" data-question="4">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">4. Há quanto tempo você sente que não dorme bem de verdade?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="menos1mes">
                        <span class="mr-3 text-xl">🔘</span> Menos de 1 mês
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="1a6meses">
                        <span class="mr-3 text-xl">🔘</span> De 1 a 6 meses
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="6a12meses">
                        <span class="mr-3 text-xl">🔘</span> De 6 meses a 1 ano
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="mais1ano">
                        <span class="mr-3 text-xl">🔘</span> Mais de 1 ano
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sempre tive problemas com o sono
                    </button>
                </div>
                <p class="text-sm text-blue-200 mt-4 italic">(Traz a dor à tona, mas de forma leve e reflexiva. Faz a pessoa pensar no impacto acumulado.)</p>
            </div>

            <!-- Pergunta 5 -->
            <div class="question" data-question="5">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">5. Se você pudesse mudar uma coisa no seu sono hoje, o que seria?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="dormir_rapido">
                        <span class="mr-3 text-xl">🔘</span> Dormir mais rápido
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="parar_acordar">
                        <span class="mr-3 text-xl">🔘</span> Parar de acordar no meio da noite
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="energia">
                        <span class="mr-3 text-xl">🔘</span> Acordar com mais energia
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="tudo">
                        <span class="mr-3 text-xl">🔘</span> Tudo isso!
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nao_sei">
                        <span class="mr-3 text-xl">🔘</span> Não sei ao certo
                    </button>
                </div>
            </div>

            <!-- Pergunta 6 -->
            <div class="question" data-question="6">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">6. Quantas horas você normalmente dorme por noite?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="menos5">
                        <span class="mr-3 text-xl">🔘</span> Menos de 5 horas 😴
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="5a6">
                        <span class="mr-3 text-xl">🔘</span> Entre 5 e 6 horas
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="6a7">
                        <span class="mr-3 text-xl">🔘</span> Entre 6 e 7 horas
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="7a8">
                        <span class="mr-3 text-xl">🔘</span> Entre 7 e 8 horas
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="mais8">
                        <span class="mr-3 text-xl">🔘</span> Mais de 8 horas
                    </button>
                </div>
            </div>

            <!-- Pergunta 7 -->
            <div class="question" data-question="7">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">7. Com que frequência você se sente cansado(a) durante o dia?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Todos os dias, constantemente 🥱
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="frequente">
                        <span class="mr-3 text-xl">🔘</span> Frequentemente, quase todos os dias
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes, algumas vezes na semana
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente, poucas vezes ao mês
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Quase nunca me sinto cansado(a)
                    </button>
                </div>
            </div>

            <!-- Pergunta 8 -->
            <div class="question" data-question="8">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">8. Você usa eletrônicos (celular, TV, tablet) até momentos antes de dormir?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sim, todas as noites 📱
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="frequente">
                        <span class="mr-3 text-xl">🔘</span> Frequentemente, quase todas as noites
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Nunca uso eletrônicos antes de dormir
                    </button>
                </div>
            </div>

            <!-- Pergunta 9 -->
            <div class="question" data-question="9">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">9. O que você costuma fazer quando não consegue dormir?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="celular">
                        <span class="mr-3 text-xl">🔘</span> Mexo no celular/tablet/computador
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="tv">
                        <span class="mr-3 text-xl">🔘</span> Assisto TV
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="ler">
                        <span class="mr-3 text-xl">🔘</span> Leio um livro
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="meditar">
                        <span class="mr-3 text-xl">🔘</span> Pratico técnicas de relaxamento/meditação
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="fico_na_cama">
                        <span class="mr-3 text-xl">🔘</span> Fico na cama tentando dormir, mesmo sem sono
                    </button>
                </div>
            </div>

            <!-- Pergunta 10 -->
            <div class="question" data-question="10">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">10. Você já experimentou alguma destas técnicas para melhorar seu sono?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="medicamentos">
                        <span class="mr-3 text-xl">🔘</span> Medicamentos para dormir
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="meditacao">
                        <span class="mr-3 text-xl">🔘</span> Meditação ou técnicas de respiração 🧘
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="rotina">
                        <span class="mr-3 text-xl">🔘</span> Rotina de sono consistente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="chás">
                        <span class="mr-3 text-xl">🔘</span> Chás ou suplementos naturais
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nenhuma">
                        <span class="mr-3 text-xl">🔘</span> Nenhuma dessas técnicas
                    </button>
                </div>
            </div>

            <!-- Pergunta 11 -->
            <div class="question" data-question="11">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">11. Como você classificaria a qualidade do seu quarto para dormir?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="excelente">
                        <span class="mr-3 text-xl">🔘</span> Excelente - escuro, silencioso e com temperatura agradável
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="boa">
                        <span class="mr-3 text-xl">🔘</span> Boa - tem alguns elementos ideais para o sono
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="regular">
                        <span class="mr-3 text-xl">🔘</span> Regular - poderia melhorar em vários aspectos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="ruim">
                        <span class="mr-3 text-xl">🔘</span> Ruim - tem muitos problemas (barulho, luz, temperatura inadequada)
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="pessima">
                        <span class="mr-3 text-xl">🔘</span> Péssima - é quase impossível ter um bom sono neste ambiente
                    </button>
                </div>
            </div>

            <!-- Pergunta 12 -->
            <div class="question" data-question="12">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">12. Você consome cafeína (café, chá, refrigerantes, energéticos) após as 14h?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sim, todos os dias ☕
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="frequente">
                        <span class="mr-3 text-xl">🔘</span> Frequentemente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Nunca consumo cafeína após às 14h
                    </button>
                </div>
            </div>

            <!-- Pergunta 13 -->
            <div class="question" data-question="13">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">13. Qual sua principal motivação para melhorar seu sono?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="energia">
                        <span class="mr-3 text-xl">🔘</span> Ter mais energia durante o dia ⚡
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="produtividade">
                        <span class="mr-3 text-xl">🔘</span> Melhorar minha produtividade
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="saude">
                        <span class="mr-3 text-xl">🔘</span> Cuidar melhor da minha saúde
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="disposicao">
                        <span class="mr-3 text-xl">🔘</span> Ter mais disposição para atividades que gosto
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="humor">
                        <span class="mr-3 text-xl">🔘</span> Melhorar meu humor e relacionamentos
                    </button>
                </div>
            </div>

            <!-- Pergunta 14 -->
            <div class="question" data-question="14">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">14. Você mantém horários regulares para dormir e acordar?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sim, todos os dias, inclusive fins de semana ⏰
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="diasuteis">
                        <span class="mr-3 text-xl">🔘</span> Sim, nos dias úteis, mas não nos fins de semana
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes, não é muito regular
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente sigo uma rotina
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Nunca tenho horários regulares
                    </button>
                </div>
            </div>

            <!-- Pergunta 15 -->
            <div class="question" data-question="15">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">15. Você pratica atividade física regularmente?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="diariamente">
                        <span class="mr-3 text-xl">🔘</span> Sim, diariamente 🏃‍♂️
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="3a5">
                        <span class="mr-3 text-xl">🔘</span> Sim, 3-5 vezes por semana
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="1a2">
                        <span class="mr-3 text-xl">🔘</span> Sim, 1-2 vezes por semana
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente me exercito
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Não pratico nenhuma atividade física
                    </button>
                </div>
            </div>

            <!-- Pergunta 16 -->
            <div class="question" data-question="16">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">16. Você costuma acordar no meio da noite?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sim, várias vezes todas as noites
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="frequente">
                        <span class="mr-3 text-xl">🔘</span> Frequentemente, quase todas as noites
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes, algumas noites por semana
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente acordo no meio da noite
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Quase nunca acordo durante a noite
                    </button>
                </div>
            </div>

            <!-- Pergunta 17 -->
            <div class="question" data-question="17">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">17. Você se sente renovado(a) quando acorda pela manhã?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="sempre">
                        <span class="mr-3 text-xl">🔘</span> Sim, sempre me sinto renovado(a) 💫
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="frequente">
                        <span class="mr-3 text-xl">🔘</span> Frequentemente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="as_vezes">
                        <span class="mr-3 text-xl">🔘</span> Às vezes
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="raramente">
                        <span class="mr-3 text-xl">🔘</span> Raramente
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nunca">
                        <span class="mr-3 text-xl">🔘</span> Nunca me sinto renovado(a) ao acordar
                    </button>
                </div>
            </div>

            <!-- Pergunta 18 -->
            <div class="question" data-question="18">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">18. Quanto tempo você geralmente leva para adormecer?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="menos5">
                        <span class="mr-3 text-xl">🔘</span> Menos de 5 minutos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="5a15">
                        <span class="mr-3 text-xl">🔘</span> Entre 5 e 15 minutos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="15a30">
                        <span class="mr-3 text-xl">🔘</span> Entre 15 e 30 minutos
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="30a60">
                        <span class="mr-3 text-xl">🔘</span> Entre 30 minutos e 1 hora
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="mais60">
                        <span class="mr-3 text-xl">🔘</span> Mais de 1 hora
                    </button>
                </div>
            </div>

            <!-- Pergunta 19 -->
            <div class="question" data-question="19">
                <h2 class="text-xl md:text-2xl font-semibold mb-6">19. Você já recebeu algum diagnóstico relacionado ao sono?</h2>
                <div class="grid gap-4">
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="insonia">
                        <span class="mr-3 text-xl">🔘</span> Insônia
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="apneia">
                        <span class="mr-3 text-xl">🔘</span> Apneia do sono
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="outro">
                        <span class="mr-3 text-xl">🔘</span> Outro transtorno do sono
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="suspeita">
                        <span class="mr-3 text-xl">🔘</span> Suspeito que tenho, mas não fui diagnosticado(a)
                    </button>
                    <button class="option-btn py-3 px-4 rounded-lg text-left flex items-center" data-value="nao">
                        <span class="mr-3 text-xl">🔘</span> Não, nunca recebi nenhum diagnóstico
                    </button>
                </div>
            </div>

            <!-- Formulário Final -->
            <div class="question" data-question="20">
                <div class="text-center mb-8">
                    <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/svg/1f4a4.svg" alt="Sono" class="sleep-icon mx-auto mb-4" style="width: 64px; height: 64px;">
                    <h2 class="text-2xl md:text-3xl font-bold mb-2">Estamos quase lá!</h2>
                    <p class="text-lg text-blue-100">Parabéns por completar o quiz! Com base nas suas respostas, preparamos um plano personalizado para transformar seu sono.</p>
                </div>

                <div class="bg-white/10 p-6 rounded-xl backdrop-blur-sm">
                    <h3 class="text-xl font-semibold mb-4 text-center">Para onde devemos enviar seu plano personalizado de Sono Primordial?</h3>
                    
                    <form id="lead-form" class="space-y-5">
                        <div>
                            <label for="name" class="block text-sm font-medium mb-1">Seu nome:</label>
                            <input type="text" id="name" name="name" required class="w-full px-4 py-3 bg-white/10 rounded-lg border border-blue-300/30 focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-blue-200/70" placeholder="Digite seu nome completo">
                        </div>
                        
                        <div>
                            <label for="email" class="block text-sm font-medium mb-1">Seu melhor e-mail:</label>
                            <input type="email" id="email" name="email" required class="w-full px-4 py-3 bg-white/10 rounded-lg border border-blue-300/30 focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-blue-200/70" placeholder="exemplo@email.com">
                        </div>
                        
                        <div>
                            <label for="whatsapp" class="block text-sm font-medium mb-1">WhatsApp (opcional):</label>
                            <input type="tel" id="whatsapp" name="whatsapp" class="w-full px-4 py-3 bg-white/10 rounded-lg border border-blue-300/30 focus:outline-none focus:ring-2 focus:ring-white/50 text-white placeholder-blue-200/70" placeholder="(00) 00000-0000">
                        </div>
                        
                        <button type="submit" id="submit-form" class="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-6 rounded-lg transition duration-300 shadow-lg transform hover:translate-y-[-2px] flex items-center justify-center">
                            <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/svg/1f4a4.svg" alt="Sono" class="mr-2" style="width: 24px; height: 24px;">
                            Receber Meu Plano Personalizado
                        </button>
                    </form>
                    
                    <p class="text-xs text-center mt-4 text-blue-200">Ao clicar em "Receber Meu Plano Personalizado", você concorda em receber comunicações sobre o Sono Primordial e outros produtos relacionados ao seu bem-estar. Você pode cancelar a qualquer momento.</p>
                </div>
            </div>

            <!-- Tela de Sucesso -->
            <div class="question" data-question="21">
                <div class="text-center py-8">
                    <div class="flex justify-center mb-6">
                        <div class="relative">
                            <div class="absolute inset-0 rounded-full bg-indigo-500/20 animate-pulse"></div>
                            <div class="relative">
                                <svg class="w-24 h-24 text-indigo-400" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12Z" stroke="currentColor" stroke-width="2"/>
                                    <path d="M8 12L11 15L16 9" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                                </svg>
                            </div>
                        </div>
                    </div>

                    <h2 class="text-3xl font-bold mb-4">Sucesso!</h2>
                    <p class="text-xl text-blue-100 mb-6">Seu plano personalizado de Sono Primordial foi enviado para seu e-mail.</p>
                    <p class="text-lg text-blue-200 mb-8">Verifique sua caixa de entrada nos próximos minutos e prepare-se para transformar suas noites de sono!</p>
                    <p class="text-sm text-blue-300">Se não encontrar o e-mail, verifique sua pasta de spam ou promoções.</p>

                    <div class="mt-10 max-w-md mx-auto">
                        <div class="bg-white/10 rounded-xl p-6 backdrop-blur-sm">
                            <div class="flex items-center mb-4">
                                <img src="https://cdn.jsdelivr.net/gh/twitter/twemoji@14.0.2/assets/svg/1f4a4.svg" alt="Sono" class="mr-3" style="width: 24px; height: 24px;">
                                <h3 class="text-lg font-semibold">Dica rápida:</h3>
                            </div>
                            <p class="text-blue-100">Comece hoje mesmo estabelecendo um horário fixo para dormir e acordar, mesmo nos fins de semana. Esta simples mudança pode melhorar drasticamente a qualidade do seu sono!</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
