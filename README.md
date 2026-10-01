# MesaBoa — V2

## Proposta
Assistente pessoal de planejamento de refeições e eventos: receitas → cardápio → convidados → bebidas → compras → custos.

## Funcionalidades de produto
- Biblioteca de receitas com rendimento original.
- Dimensionamento automático.
- Eventos com adultos e crianças.
- Assistente de IA para sugerir cardápios usando receitas salvas.
- Bebidas como módulo contextual: a recomendação considera prato, ocasião, duração, clima e perfil dos convidados, em vez de depender apenas de uma regra fixa.
- Bebidas alcoólicas são tratadas como opções exclusivamente para convidados adultos; crianças recebem planejamento de opções sem álcool.
- Lista de compras consolidada.
- Preços, custo total e custo por pessoa.
- Importação de receitas por URL com tela de revisão antes de salvar.
- Fonte original preservada.
- PWA instalável.

## Arquitetura de dados planejada
Recipe
Ingredient
Event
GuestProfile
Menu
MenuItem
Drink
ShoppingItem
Price
ImportSource

## Fluxo
1. Criar evento ou pedir inspiração.
2. Informar adultos/crianças e contexto.
3. IA sugere um cardápio a partir do acervo.
4. Usuário revisa e confirma.
5. Receitas são dimensionadas.
6. Bebidas são recomendadas conforme o contexto.
7. Ingredientes são consolidados.
8. Lista de compras e custos são gerados.

## Importação de receitas
A integração final deve tentar ler URLs públicas e extrair título, rendimento, ingredientes, quantidades, preparo, autor e fonte. Conteúdo inacessível deve oferecer fallback por texto ou imagem. Nunca salvar automaticamente sem revisão.

## Observação
Este pacote é um protótipo front-end. A IA real, sincronização e banco de dados ainda precisam ser conectados.
