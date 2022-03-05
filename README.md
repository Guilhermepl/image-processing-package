# Projeto: Pacote de Processamento de Imagens
## Autora do Projeto: Karina Kato
### Aula: Descomplicando a criação de pacotes de processamento de imagens em Python - Digital Innovation One
[(clique aqui para ver o meu perfil na plataforma)](https://web.digitalinnovation.one/users/limapeguilherme)
#### Tecnologia: Python
#### Data: 05/03/2022
-----------------------------------------
### Descrição
O pacote "image_processing-test" é usado para:

- Módulo "Processing":
  - Correspondência de histograma;
  - Similaridade estrutural;
  - Redimensionar imagem;

- Módulo "Utils":
  - Ler imagem;
  - Salvar imagem;
  - Plotar imagem;
  - Resultado do gráfico;
  - Plotar histograma;
---------------------------------------------
## Passo a passo da configuração para hospedar um pacote em Python no ambiente de testes Test Pypi

- [x] Instalação das últimas versões de "setuptools" e "wheel"

```
py -m pip install --user --upgrade setuptools wheel
```
- [x] Tenha certeza que o diretório no terminal seja o mesmo do arquivo "setup.py"

```
C:\User\Henrique\image-processing-package> py setup.py sdist bdist_wheel
```

- [x] Após completar a instalação, verifique se as pastas abaixo foram adicionadas ao projeto:
  - [x] build;
  - [x] dist;
  - [x] image_processing_test.egg-info.

- [x] Basta subir os arquivos, usando o Twine, para o Test Pypi:

```
py -m twine upload --repository testpypi dist/*
```

- [x] Após rodar o comando acima no terminal, será pedido para inserir o usuário e senha. Feito isso, o projeto estará hospedado no Test Pypi.hospedá-lo no Pypi diretamente.

----------------------------------------------------
## Instalação local, após hospedagem no Test Pypi

- [x] Instalação de dependências
```
pip install -r requirements.txt
```

- [x] Instalção do Pacote

Use o gerenciador de pacotes ```pip install -i https://test.pypi.org/simple/ image-processing-test ```para instalar image_processing-test

```bash
pip install image-processing-test
```
-------------------------------------------------
## Como usar em qualquer projeto

```python
from image-processing-test.processing import combination
combination.find_difference(image1, image2)
```
<img width="auto" src="https://github.com/HenriqueMAP/image-processing-package/blob/master/image-processing-test.png?raw=true">

## Autor (quem hospedou o projeto no Test Pypi)
Guilherme Pereira Lima

## Licença
[MIT](https://choosealicense.com/licenses/mit/)
