Progresso da Caixa de Fósforos — Calculadora de NEX
Ferramenta de mesa para acompanhar o Nível de Exposição Paranormal (NEX) das cobaias de uma campanha de RPG no sistema Ordem Paranormal. Site estático, sem servidor, pensado para o mestre registrar a evolução de cada personagem ao longo das sessões.
Estética alinhada ao universo da campanha: tipografia Metal Mania e Shadows Into Light Two, paleta amarelo-backrooms sobre o papel de parede verde dos corredores, com luz fluorescente doente.
O que faz

Mostra as 7 cobaias (FHP 001 a 007), cada uma com o NEX inicial e o nome.
Aba "Aumento de NEX" por personagem, com os cinco gatilhos de exposição. Um clique aplica o aumento.
Reverter qualquer aumento, tanto pelo botão "desfazer último" no card quanto pelo "reverter" de cada registro no histórico.
Página de Histórico com todos os aumentos, em ordem cronológica, mostrando data, hora, cobaia, causa, valor somado e NEX resultante. Tem filtro por personagem.
O número do NEX muda de cor conforme sobe (amarelo, âmbar, laranja, sangue, hematoma), funcionando como medidor de contaminação.
Exportar / Importar backup em JSON, para guardar o progresso e levar para outro aparelho.

NEX inicial das cobaias
CobaiaNomeNEXFHP 001Faca11%FHP 002Sabonete10%FHP 003Mostarda22%FHP 004Papelão20%FHP 005Papel15%FHP 006Luva11%FHP 007Velcro24%
Gatilhos de aumento
GatilhoNEXExposição à criatura+2Exposição leve à sala de medo+2Exposição moderada à sala de medo+3Aprender Ritual+1Transcender+1
O NEX é limitado entre 0% e 99%.
Arquivos

index.html — o site inteiro (HTML, CSS e JavaScript em um arquivo só).
backrooms.png — imagem de fundo (papel de parede dos backrooms).

Os dois ficam lado a lado na raiz do repositório.
Como publicar no GitHub Pages

Crie um repositório novo (por exemplo, caixa-de-fosforos).
Suba index.html e backrooms.png na raiz.
Vá em Settings > Pages, em Branch selecione main e a pasta / (root), e salve.
Aguarde alguns instantes e acesse a URL gerada (algo como https://SEU-USUARIO.github.io/caixa-de-fosforos/).

Como usar

Na aba Calculadora, abra o "Aumento de NEX" da cobaia desejada.
Clique no gatilho que ocorreu na sessão. O NEX é somado na hora e o evento entra no histórico com a data.
Errou ou foi só teste? Use "desfazer último" no card, ou "reverter" no registro específico dentro do Histórico.
De tempos em tempos, use Exportar backup para salvar o progresso da campanha.

Onde mexer para personalizar
Tudo está dentro do index.html.

NEX inicial e nomes: no bloco const COBAIAS (no <script>).
Gatilhos e valores: no bloco const GATILHOS. Dá para mudar valores, renomear ou acrescentar novos.
Tamanho do padrão da parede: no body, propriedade background-size: 300px.
Quanto o fundo escurece: no body, o linear-gradient logo acima da imagem.
Cores do NEX por faixa: na função corNex.

Persistência
Os dados ficam salvos no navegador (localStorage), não em um servidor. Isso significa que:

O progresso é por aparelho e por navegador. Para sincronizar entre celular e computador, use os botões de exportar e importar backup.
Limpar os dados do navegador apaga o histórico. Mantenha um backup recente.

Se no futuro for necessário sincronizar automaticamente entre vários aparelhos, a calculadora pode ser ligada a um backend leve (Cloudflare Worker com KV), como já é feito no site da Parede de Desejos.
Tecnologia
HTML, CSS e JavaScript puro, sem dependências além das fontes do Google Fonts. Não há build nem servidor.
