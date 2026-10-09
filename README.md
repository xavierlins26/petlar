# PetLar — plataforma de adoção responsável

Site responsivo de adoção responsável, desenvolvido com HTML5, CSS3 e JavaScript puro.

## Organização: cada página tem seu próprio HTML
- `index.html`: página inicial, banner, busca, categorias, destaques e ONGs parceiras.
- `animais.html`: catálogo de 15 animais anunciados por pessoas.
- `animal-detalhes.html`: detalhes do animal selecionado pela URL (`?id=...`).
- `ongs.html`: catálogo com 5 ONGs demonstrativas.
- `ong-detalhes.html`: perfil da ONG selecionada pela URL (`?id=...`).
- `animais-ong.html`: catálogo individual de cada ONG, com 15 animais por organização (75 animais demonstrativos no total).
- `favoritos.html`, `perfil.html`, `login.html`, `cadastro.html`, `cadastrar-animal.html`, `como-funciona.html`, `sobre.html` e `contato.html`: páginas independentes para as outras funções.

## Organização dos arquivos
- `css/global.css`: estilo compartilhado e identidade visual.
- `css/icones.css`: regras compartilhadas para manter tamanho, traço e alinhamento dos ícones padronizados.
- Outros arquivos em `css/`: estilos específicos por página.
- `js/dados.js`: dados de demonstração dos animais e das ONGs. É o principal arquivo para editar nomes, características, fotos e vínculos.
- Outros arquivos em `js/`: interações separadas por funcionalidade.
- `assets/imagens/`: local sugerido para colocar suas imagens.
- `assets/videos/pets-demo.mp4`: caminho esperado para o vídeo de fundo do banner.

## Como executar
1. Extraia o ZIP.
2. Abra a pasta `PetLar` no Visual Studio Code.
3. Abra `index.html` no navegador ou use a extensão Live Server.
4. Edite os dados em `js/dados.js` e as fotografias nos dados/HTML correspondentes.

## Ícones padronizados
Os ícones são vetoriais (SVG), sem emojis, com traço e dimensões controlados por `css/icones.css`. Para manter o padrão, prefira SVGs com `viewBox="0 0 24 24"`, `fill="none"`, `stroke="currentColor"`, `stroke-width="1.8"`, `stroke-linecap="round"` e `stroke-linejoin="round"`.

## Importante
- Os animais, ONGs, números e comentários são demonstrativos, não são anúncios nem organizações verificadas.
- As fotografias de demonstração vêm de URLs externas; é necessária conexão com a internet. Substitua-as por fotos que você tenha autorização para usar.
- Favoritos ficam no `localStorage` deste navegador.
- Cadastro, login, contato e publicação não armazenam dados em servidor. Para uso real, será necessário backend, autenticação segura, validação no servidor, proteção de dados e moderação.
- Os links oficiais das ONGs estão vazios intencionalmente; preencha somente endereços confirmados.


## Chat e acesso
- `chat.html`, `css/chat.css` e `js/chat.js` formam um chat demonstrativo local. Para mensagens reais, conecte-o a um backend/API e ao banco de dados.
- `login.html` não simula autenticação. Integre-o ao serviço de autenticação seguro quando o backend estiver pronto.


Acesso demonstrativo local: manusilva@gmail.com / 12345. O login e os cadastros de demonstração usam o armazenamento local do navegador; para uso público, substitua por autenticação segura no servidor.


Acesso demonstrativo local: manusilva@gmail.com / 12345. O login e os cadastros de demonstração usam o armazenamento local do navegador; para uso público, substitua por autenticação segura no servidor.


## Atualização visual
A página inicial agora usa fotografia de fundo, paleta mais colorida e três categorias ilustradas (cachorros, gatos e outros animais). Os formulários têm campos alinhados e controles de senha com ícone de olho. As páginas de ações (catálogo, favoritos, perfil, cadastro de pet e chat) pedem acesso primeiro. A autenticação continua demonstrativa no navegador e deverá ser substituída por autenticação segura no backend ao publicar o projeto.


## Regras de acesso desta versão
- Início, Sobre nós, Como funciona, Contato e cadastro de conta são páginas públicas.
- Animais, ONGs, chat, favoritos, perfil, detalhes e cadastro de animais exigem sessão local e redirecionam ao login.
- Favoritar um pet na página inicial também solicita login.
- O acesso demonstrativo usa armazenamento local; antes de publicar, conecte uma autenticação segura e o banco de dados.


## Recursos desta versão
- Categorias para cachorros, gatos, coelhos e aves; a opção **Outros** filtra espécies que não sejam cão ou gato.
- Cadastro de animal com foto, idade, sexo, porte, pelagem, cor, olhos, vacinação, castração, descrição e contato.
- Publicações aparecem na aba Animais e no perfil do usuário, usando armazenamento local do navegador.
- Formulário de avaliação de ONG após adoção, com notas e comentários guardados localmente.

**Nota técnica:** esta versão é funcional para demonstração em um navegador. Contas, publicações, fotos e avaliações ficam no armazenamento local e não são compartilhadas entre dispositivos. Para uso público real, conecte autenticação e banco de dados.


## Atualização visual e navegação
- Agora, apenas as páginas de login e cadastro ficam públicas. Ao abrir qualquer outra página sem sessão, o visitante é enviado para o login antes de a página aparecer.
- Depois do login, o perfil é a página padrão; se a pessoa foi encaminhada para uma página interna específica, pode continuar para esse destino.
- A interface ganhou cores mais vivas, patinhas decorativas e animações suaves, respeitando a preferência de movimento reduzido.
- No perfil, cada animal publicado tem um seletor de status: Disponível, Adoção em processo ou Adotado.
- Para encaminhar ao anúncio oficial de uma ONG, preencha `adoptionUrl` no objeto do animal em `js/dados.js`. Como alternativa, o código usa `site` da ONG. Os comentários `LINKAR ANÚNCIO OFICIAL DA ONG` indicam o local.
- Foto, perfil, anúncios e status ainda são guardados no armazenamento local do navegador; para autenticação segura e compartilhamento entre pessoas, conecte ao backend real.


### Atualizações recentes
- Cadastro e edição aceitam até três fotos por animal; a galeria mostra apenas as fotos realmente enviadas.
- Na conta, cada anúncio pode ser editado, excluído e ter o status atualizado.
- O contato do responsável permite WhatsApp/telefone ou e-mail.
- Para contato direto com uma ONG, configure `adoptionUrl` no registro do animal em `js/dados.js` (ou `site` no registro da ONG).
