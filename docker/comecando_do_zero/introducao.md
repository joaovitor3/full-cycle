# Containers

Container, é um processo com subprocessos rodando emulando um sistema operacional.
O container utiliza um processo e as dependências de kernel rodam em sistema operacional

## Namespace

Responsável por isolar processos

- processo pai container 1
    - n processos filhos container 1
- processo pai container 2
    - n processos filhos container 2

## Cgroups

Controla os recursos computacionais do container

## File System

OFS (Overlay File System)
- Trabalha com camadas (layers) e apenas armazena cópias de diferenças de versões

## Imagens

Utiliza a ideia de trabalhar com camadas de dependências e as dependências podem ser reutilizadas em outras imagens.

É um conjunto de dependências amarradas que possuem um nome (tag).

Possui estado imutável, ou seja não é alterada após subir uma imagem. No caso, apenas podemos adicionar coisas ao rodar comandos dentro de um container.

É póssível realizar o commit dentro de um container que realiza a geração de uma nova imagem a partir do que está dentro da imagem

## Dockerfile

Arquivo declarativo de uma imagem

FROM - comando para baixar imagem
RUN - roda comando na imagem
EXPOSE - expõe as portas

## Armazenamento de imagens

Registry

Posso dar pull e push de imagens

## Docker Host

### Daemon

Possui um host onde roda o docker, que roda um processo (daemon) que disponibiliza uma API para trabalhar com o Docker. Essa API disponibilizada pelo Daemon é chamada pelo Docker Client - quando digitamos docker `<comando>` 

### Cache

Adiciona camada de cache para dependências de imagens

### Volumes

Utilizado para persistir dados de um container

### Network

Comunicação entre containers