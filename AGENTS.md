# AGENTS.md

Este repositório é um app Flutter com autenticação Firebase e foco em telas de login, cadastro e recuperação de senha.

## Visão rápida
- App principal em `lib/main.dart`
- Fluxo de autenticação em `lib/login.dart`, `lib/sign.dart`, `lib/forgot.dart`
- Configuração do Firebase em `lib/firebase_options.dart`
- Estilo e navegação com widgets Material do Flutter

## Comandos úteis
- Instalar dependências: `flutter pub get`
- Executar no navegador: `flutter run -d chrome`
- Executar em modo web local com porta explícita: `flutter run -d chrome --web-port 8080`
- Rodar testes: `flutter test`
- Verificar análise estática: `flutter analyze`

## Arquitetura e convenções
- `main.dart` inicializa o Firebase e define o `AuthGate` para redirecionar usuários autenticados e não autenticados.
- O fluxo principal usa `FirebaseAuth.instance` para login, criação de conta e recuperação de senha.
- A UI é organizada em arquivos separados por tela, seguindo estrutura simples e sem bloc/riverpod.
- O app foi criado como projeto padrão Flutter, então a lógica de estado fica muito perto dos widgets.

## Observações para web
- Para visualizar a aparência web, use o canal `chrome` do Flutter; a aplicação pode ser inspecionada e ajustada pelo navegador.
- O app depende da configuração do Firebase no web; confirme que `firebase_options.dart` e os arquivos de configuração do Firebase estão consistentes com o projeto.
- A experiência de desktop/web é guiada por widgets Material e o layout deve considerar largura máxima e responsividade em formulários.

## Dicas para agentes de IA
- Preferir mudanças pequenas e localizadas nas telas em `lib/`.
- Ao alterar autenticação, verificar o efeito em `AuthGate` e nas telas de login/cadastro.
- Se a mudança for de layout, priorizar `ConstrainedBox`, `Padding`, `Row`/`Column` e responsividade para manter aparência consistente no web.
- Não reinventar o projeto; seguir o padrão já usado em cada tela e manter nomes em português/consistentes com o app.

## Links relevantes
- [README.md](README.md)
- [lib/main.dart](lib/main.dart)
- [lib/login.dart](lib/login.dart)
- [lib/sign.dart](lib/sign.dart)
- [lib/forgot.dart](lib/forgot.dart)
- [lib/firebase_options.dart](lib/firebase_options.dart)
