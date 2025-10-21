O que é o AWS Step Functions?
É um serviço da AWS que permite montar fluxos de trabalho automatizados, onde cada etapa executa uma ação. Ele ajuda a conectar vários serviços da AWS, como Lambda, S3, DynamoDB, etc., de forma organizada.
Você escreve esse fluxo como uma espécie de "roteiro", usando uma linguagem chamada Amazon States Language (ASL).

Principais Elementos do Step Functions
State Machine: é o fluxo completo. Define as etapas e como elas se conectam.

Estados: são as etapas do fluxo. Cada uma faz algo específico.
Task: executa uma tarefa (como rodar uma função Lambda).
Choice: faz uma escolha com base em alguma condição (como um if).
Parallel: roda várias coisas ao mesmo tempo.
Map: repete uma tarefa para vários itens (como um for).
Pass: só passa os dados pra frente, sem mudar nada.
Wait: espera um tempo antes de continuar.
Succeed / Fail: finaliza o fluxo com sucesso ou erro.

Como os dados circulam

InputPath: escolhe o que da entrada será usado.
ResultPath: define onde guardar o resultado da etapa.
OutputPath: escolhe o que será passado para a próxima etapa.

Isso é útil quando você quer controlar o que vai e volta em cada etapa do fluxo.
Serviços que dá pra usar juntos
Você pode integrar o Step Functions com vários serviços, como:

Lambda (para lógica de negócio)
S3 (para salvar ou pegar arquivos)
DynamoDB (para gravar ou ler dados)
SNS/SQS (para enviar mensagens)
ECS ou Batch (para tarefas mais pesadas)
