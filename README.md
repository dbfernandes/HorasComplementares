# Sistema de Horas Complementares do IComp/UFAM

Código do sistema de gerenciamento horas complementares da graduação do Instituto de Computação da UFAM. Professores responsáveis pelo código: David Fernandes de Oliveira e Arilo Cláudio Dias-Neto.

## Como contribuir

Para contribuir com este trabalho, crie um fork deste projeto em sua conta no Github e submeta suas contribuições através de Pull Requests. Esse fork deve ser feito a partir do repositório original, que pode ser acessado através do endereço abaixo:

```
https://github.com/dbfernandes/HorasComplementares
```

## Como instalar este sistema

O primeiro passo para instalação é fazer um fork do repositório original do sistema em sua conta do Github. Para fazer isso, acesse endereço (https://github.com/dbfernandes/HorasComplementares) e click o botão fork desse repositório (vide imagem abaixo).

![Fork no Github](http://coyote.icomp.ufam.edu.br/sysicomp/fork.png)

Após o fork, você pode clonar seu novo repositório através do comando git clone:

```
$ git clone https://github.com/<seu usuário no github>/HorasComplementares
```

Feito o clone, basta seguir as orientações de instalação de qualquer sistema desenvolvido através do Yii 2. O primeiro passo é instalar as dependências do sistema através do composer:

```
$ php composer.phar install
```

Depois disso, acesse a turma de **Prática de Banco de Dados** no **CodeBench** (2017/2), clique na aba de Materiais Didáticos, e faça o download do Dump do banco de dados do deste sistema. Esse Dump foi gerado a partir do sistema em produção, e foi colocado no Codebench porque possui dados sigilosos.

Crie um banco de dados MySQL em seu sistema e carregue o dump no novo banco. Crie um arquivo chamado `db.php` dentro do diretório `config` com o seguinte conteúdo:

```
<?php

return [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=<banco>',
    'username' => '<usuario do banco>',
    'password' => '<senha usuario do banco>',
    'charset' => 'utf8',
];
```

No arquivo `db.php`, troque as strings `<banco>`, `<usuario do banco>` e `<senha usuario do banco>` pelos dados corretos dentro de seu sistema.

Para acessar o backend, você pode usar o seguinte usuário:

```
Nome Completo: Usuário Todo Poderoso
CPF: 362.687.674-89
Senha: Utp102030
```
