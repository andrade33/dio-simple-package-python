
1. Criar um projeto

2. Editar "setup.py", "requirements.txt" e "README.md" e gerar "wheel" e "sdist".

Para isso:
3. Acessar a raiz e roda os comandos

python -m pip install --upgrade pip
python -m pip install --user twine
python -m pip install --user setuptools
pip install wheel

5. Comando para criar distribuicao
python setup.py sdist bdist_wheel

6. Publicar pacote
Necessário conta no Test Pypi e no Pypi 

Test Pypi
Pypi

python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*
6.2. Agora, instale o pacote de teste:
pip install -i https://test.pypi.org/simple/ image_exercise
Pypi
6.3. Com tudo testado, e hora de publicar o pacote no Pypi:
python -m twine upload --repository-url https://upload.pypi.org/legacy/ dist/*
6.4. Instale o pacote publicado:
Utilize o gerenciador de pacotes pip para instalar image_exercise

pip install image-exercise

================================
Obs.: As imagens usadas foram excluídas do projeto.
