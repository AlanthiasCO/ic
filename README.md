# Projeto: Mosquito

## Projeto em andamento - README desatualizado.

Resumo: Este projeto visa a utilização de modelos de aprendizagem (ML) para a classificação de áudios de mosquitos. 
No momento, apenas os espectrogramas estão sendo utilizados para a classificação mas pretendo utilizar outras formas, p.ex: MFCC.

## Etapas realizadas

#### Tipos de Mosquitos: Os áudios de mosquitos coletados pelo Projeto HumBug:

- Grupo A: Culex Quinquefasciatus.
- Grupo B: Anopheles Gambiae.
- Grupo C: Aedes Aegypti e Aedes albopictus.
- Grupo D: Anopheles Barbirostris e Anopheles Maculatus.

Fonte: https://humbug.ox.ac.uk/article/new-publication


#### Seleção: Espécies de mosquitos comuns no Brasil, que estão presentes no repositório HumBug Zooniverse:

- Grupo A: Culex Quinquefasciatus
- Grupo B: Anopheles Gambiae
- Grupo C: Aedes Aegypti
- Grupo D: Nenhum

Quantidade de áudios de mosquitos confirmados — apenas de espécies presentes no Brasil — no HumBug Zooniverse:

- Grupo A: 682
- Grupo B: 3.766
- Grupo C: 7.163

Foram selecionados para o Projeto apenas os grupos B e C, totalizando 10.929 áudios.

#### Equilibrando o dataset:

- O dataset está desequilibrado. O grupo C possui 3.397 áudio a mais que o grupo B, resultando em um desequilibrio muito grande. Para resolver, foi utilizado a subamostragem da classe predominante, utilizando apenas 3.766 áudios aleatórios da mesma.

Tendo agora, o dataset, um total de 7.532 áudios.

#### Feitos:
- Analise dos áudios e grupos presentes no projeto HumBug Zooniverse: a crowd-sourced acoustic mosquito dataset, definindo os mosquitos presentes em cada grupo e selecionando os que estão presentes no Brasil.
- Separação dos áudios dos dois tipos de mosquito, colocando cada tipo de áudio em um diretorio separado.
- Criação dos espectrogramas de cada tipo de mosquito.
- Criação dos dados de treino, teste e validação.
 

Próximas Etapas:
- Aplicar os espectrogramas em modelos de CNN, p.ex: VGG, ResNet
