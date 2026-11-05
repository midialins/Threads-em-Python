# Exercícios de Threads em Python

Três exercícios de programação concorrente desenvolvidos em Python para praticar o uso de threads.

As soluções utilizam `ThreadPool`, seguindo a estrutura com `main()` e `if __name__ == "__main__":` apresentada em aula. Os resultados são exibidos no terminal.

## Atividades

### Exercício 1 — Identificação das threads

Utiliza cinco threads de trabalho para executar chamadas que:

- Recebem um identificador inteiro.
- Aguardam 0,5 segundo.
- Imprimem sua identificação, como `Thread #1`.

Arquivo: `exercicio_1.py`

### Exercício 2 — Soma de valores

Realiza três somas utilizando um pool de três threads.

Cada chamada recebe:

- O identificador da linha.
- Uma lista com cinco números inteiros aleatórios de 1 a 100.

Após cada adição, a execução aguarda 0,2 segundo. Ao final, são exibidos o identificador da linha e o resultado da soma.

Arquivo: `exercicio_2.py`

### Exercício 3 — Corrida de sapos

Simula uma corrida de cinco sapos utilizando um pool de cinco threads.

Cada chamada controla um sapo e informa:

- O tamanho de cada salto.
- A distância total percorrida.
- Quando o sapo chega ao final do percurso.

Configuração utilizada:

- Percurso de 30 cm.
- Saltos aleatórios de 0 a 5 cm.
- Pausa de 0,2 segundo antes de cada salto.
- Chegada ao atingir ou ultrapassar 30 cm.

A corrida é narrada por mensagens no console.

Arquivo: `exercicio_3.py`

## Como executar

É necessário ter o Python 3 instalado. Todas as bibliotecas utilizadas fazem parte do Python.

Abra o terminal na pasta dos arquivos e execute a atividade desejada:

```bash
python3 exercicio_1.py
python3 exercicio_2.py
python3 exercicio_3.py
```

Se o seu sistema utiliza o comando `python`, substitua `python3` por `python`.

## Recursos utilizados

- `ThreadPool`: organiza um grupo de threads para executar as tarefas.
- `pool.map()`: distribui os parâmetros entre as chamadas da função e aguarda sua conclusão.
- `time.sleep()`: cria uma pausa na execução da tarefa.
- `random.randint()`: sorteia números inteiros dentro do intervalo informado.
- `main()`: organiza os parâmetros e a execução do programa.
- `if __name__ == "__main__":`: chama `main()` quando o arquivo é executado diretamente.

## Observações

A ordem das mensagens pode variar entre as execuções. Os números sorteados, os resultados das somas e a sequência de chegada dos sapos também podem mudar.

No exercício 3, o enunciado também menciona saltos de 1 a 5 cm. Para utilizar esse intervalo, altere a chamada para:

```python
random.randint(1, tamanho_maximo_pulo)
```
