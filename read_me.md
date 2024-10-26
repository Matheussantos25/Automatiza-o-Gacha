bibliotecas:

pyautogui, pillow, opencv-python
pip install pygetwindow
pip install pynput



Todas dificuldades e progressos?

Dificuldade 1: 
como captar as coordenadas todas de uma vez?

Solução 1:
Fazer um script com arquivo txt das coordenadas_salvas, assim posso copiar todos os pontos que cliquei de uma vez


Dificuldade 2:
Escolher todas as coordenadas  de que fiz na mão de forma aleatória (para face, mouth)

Solução 2:
Não adiantar captar todas as coordenadas e escolher aleatoriamente, é mais eficiente escolher aleatoriamente de forma agrupada,
assim dividi em coordenadas felizes, tristes, surpresa, etc...

Dificuldade 3:
Coordenadas mudam sempre se eu mudar a posição do jogo

Solução 3:
Deixar o jogo sempre abrir em uma coordenada específica para assim, as coordenadas que quero sejam fixas
por isso utilizei: mover_janela("Gacha Nebula", 800, 150)

Dificuldade 4: 08/10/24
Os Personagens não estavam trocando após eu consertar o problema de clicar em view, visto que  o personagem anterior
ficou clicado, mesmo se clicar 2 vezes no novo personagem não funcionou

Solução 4: 10/10/24
depois de tirar print na view fazer clicar no personagem seguinte 3 vezes (essa solução eu demorei no mínimo 4 horas pra ter)


Dificuldade 5: 10/10/24
No Gacha Nebula os balões dos personagens muito acima não fica fora da tela

Soluçao 5: 10/10/24
Criar as falas prontas como arquivo str de subtitlte e deixar o código simples para só as reações dos personagens e os prints

Dificuldade 6: 10/10/24
Não consiga simplificar o chat, as coordenadas parecem que não são mais as mesmas (mesmo sendo)

Solução 6: 10/10/24
Manter o código e deletar o texto usando a  Coordenadas capturadas: (883, 324) que é a coordenada de deletar texto, definitivamente
não é o jeito mais otimizado, já que está alongando o processo, mas foi o que deu pra fazer

Dificuldade 7: 08/10/24
O script clica nos 6 personagens, mas depois não volta de novo, ficando preso no sexto personagem

Solução 7: 11/10/24
Colocar o personagem 1 (Itadori) clicar 2 vezes e já deixar clica manualmente no itadori.

Dificuldade 8: 12/10/24
Mudança de página, faz bugar (nas posição de boca e face, são no máximo até 4 páginas), não faz sentido ter boca na posição de página acima de 4

Solução 8.1: 12/10/24
Toda vez que um personagem for trocado, resetar a página para 1 (não funcionou)

Solução 8.2: 24/10/24
Clicar o máximo de vezes na seta esquerda, não funcionou porque se clicar da página para esquerda,
o programa vai para a página 15 em mouth

Soluçaõ 8.3: 24/10/24
Rastreamento por Personagem:

Mantemos current_face_page e current_mouth_page para cada personagem.
Atualizamos essas variáveis sempre que mudamos de página.
Reset de Páginas Inteligente:

As funções reset_face_page e reset_mouth_page usam switch_face_page e switch_mouth_page para voltar à página 1 de forma eficiente.
Isso garante que sempre sabemos em qual página estamos começando para cada personagem.
Mudança de Página Otimizada:

As funções switch_face_page e switch_mouth_page calculam o número mínimo de cliques necessários para chegar à página desejada, considerando o comportamento circular.
Isso torna o script mais eficiente e evita cliques desnecessários.




Prompts poderosos:
aqui tem 6 falas, certo? gere mais que de 300 falas, lembrando que a cada 6 falas precisam ter o mesmo sentimento entre parentenses, os sentimentos são (feliz), (triste), (neutro), Itadori: "Est! (triste)" 
Nobara: "Is (triste)"
Megumi:"N (triste)"
Maki: "U (triste)"
Toge: "o (triste)"
Gojo: "S (triste)"

mande para um arquivo txt com cada frase sendo exatamente na linha de baixo


com base nisso, gere uma reação em minutagem de 6 personagens como arquivo srt, lembrando que deve ser frase curta, no máximo 5 palavras: Itadori
Nobara
Megumi 
Maki 
Toge 
Gojo