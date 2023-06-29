# Model Checking
Modelos de sistema e verificação de propriedades sobre o modelo usando a verificador de modelos NuXMV.

Este é o README.md para o código do Trabalho 2 da disciplina de Métodos Formais para Computação, desenvolvido por Caroline Lima e Joana Figueredo. O código consiste em dois módulos: "temporizador" e "main". O módulo "temporizador" implementa um temporizador com um limite de contagem de 0 a 3. O módulo "main" é o controlador principal que controla os semáforos e os sensores.


## Como testar o código usando NuSMV
Para testar o código, usaremos a ferramenta NuSMV, que é um verificador de modelagens. Siga as etapas abaixo para executar os testes.

### Pré-requisitos
Certifique-se de ter o NuSMV instalado em seu sistema. Você pode encontrar informações sobre como baixar e instalar o NuSMV em seu site oficial: http://nusmv.fbk.eu/


### Executando os testes
1. Abra o terminal ou prompt de comando e navegue até o diretório onde o NuSMV está instalado.

2. Execute o comando abaixo para iniciar o NuSMV no modo interativo.


```
NuSMV -int
```

3. No prompt do NuSMV, execute os seguintes comandos para carregar e verificar o arquivo SMV:
```
NuSMV > read_model -i main.smv
NuSMV > flatten_hierarchy
NuSMV > encode_variables
NuSMV > build_model
```

4. Para testar as propriedades especificadas no código, você pode usar o comando abaixo. Assim, será iniciada a execução do modelo.
``` 
pick_state -i
```
