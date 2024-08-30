## Порт к Static Jinja Plus


Набор докер файлов для создания образа static jinja plus

### Static  Jinja Plus


Static Jinja Plus - программа для создания статических сайтов с помощью jinja

[link](https://github.com/MrDave/StaticJinjaPlus)


### Как установить


Склонировать этот репозиторий

Образы строятся на версии python:slim(Dockerfile.slim) или ubuntu(Dockerfile.ubuntu)

Запустить

```
docker build -f Dockerfile.slim . -t [image_name]
```

С указанием версии sjp:
```
docker build -f Dockerfile.slim . -t [image_name] --build-arg VERSION=0.1.1
```


### Как использовать


```
docker run -v $(pwd)/[templates]:/app/templates -v $(pwd)/[build]:/app/build [image_name]
```

[image_name]  задается при построении образа

[templates] Папка с темплейтами

[build] Папка для записи результата

