# GitHub Scraper

Scraper de projetos abertos do GitHub, que busca a estrutura de diretórios, quantidade de linhas de cada arquivo e a porcentagem de linhas e bytes por tipo de extensão.

#### * Precisa do Python 3.6

### 1 -Instalação o projeto e suas dependências

```
git clone https://github.com/eduleones/github-scraper.git
cd github-scraper
python -m venv venv
. venv/bin/active
pip install -r requirements.txt

```


### 2 -Rodando Splash com Docker

```
sudo docker pull scrapinghub/splash
sudo docker run -p 8050:8050 -p 5023:5023 scrapinghub/splash

```

### 3 -Configurando o Splash no projeto
Editar o arquivo settings.py, e alterar para o IP que está o rodando o Splash Docker, se necessário.

```
SPLASH_URL = 'http://localhost:8050/render.html'
```

### 4 -Testando
```
pytest
```

# Como funciona

O script lê o arquivo repositories.txt que deve conter o projetos do git ( nome_usuario/projeto ) que serão analisados, exemplo de repositories.txt:

```
topics/atom
twbs/bootstrap
```

A saída dos dados será num arquivo txt que ficará na pasta 'results/'


