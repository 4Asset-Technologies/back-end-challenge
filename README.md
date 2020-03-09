# 4Asset Programming Challenge
## Rails Developer

### Geral

Na 4Asset temos várias aplicações e utilizamos Ruby e Rails para 
responder as demandas de forma rápida e com alta capacidade. Muita vezes,
quando surge um problema e não sabemos muito bem como resolve-ló, utilizamos Ruby. 

Devemos pensar em desenvolver aplicativos que façam parte de uma arquitetura maior. É preciso
capacidade de organização, documentação e abstração para conceber tais
sistemas, e é nesses aspectos que vamos mirar nessa challenge.

#### Objetivo específicos

O objetivo desse desafio é construir duas aplicações Rails. Uma com o proposito de basicamente guardar as informações no banco de dados. E a outra, com o proposito de conectar na API de streaming do Twitter e fique procurando publicações com uma determinada palavra.

#### Aplicativo para armazenar os dados

Um aplicativo Rails, extremamente simples, com um endpoint RESTful para
cadastrar novos _tweets_:

* `POST /tweets`

Ele deve validar os tweets recebidos e salvar num Banco de Dados Postgres.

No aplicativo também deve haver uma _rake task_ que traga, da maneira mais
rápida que você conseguir os seguintes dados, baseados nos tweets recebidos:

| Dado | Exemplo |
| ---- | ------- |
| Média de tweets por horário | 9:00 -> 125, 10:00 -> 200, 12:00 -> 475, ... |
| Usuário com maior número de tweets | @pedro - 25 tweets |

Simples, não?

**Extras** (não são requisitos)

* Uma boa documentação, dentro e fora do código
* Testes em RSpec (unitários e de integração)
  
#### Aplicativo para buscar os dados

Esse é o aplicativo que vai abastecer a aplicação Rails com dados do twitter.

Ele deve receber uma palavra-chave para buscar, conectar na stream _realtime_
do Twitter e passar os tweets recebidos para o aplicativo Rails.
A palavra chave pode ser passada via _environment variable_, arquivo de
configuração, _argv_, o que você quiser.

Você pode usar _gems_ para tornar a sua vida mais fácil :)

**Extras:** (não são requisitos)

* Envio assíncrono dos _tweets_ para o Rails (sem parar de receber os
  _tweets_ em realtime)
* Suporte a múltiplas palavras chave
* Gestão de indisponibilidade do app Rails com recuperação de envio
  quando o serviço voltar
* Testes em RSpec

### Requisitos técnicos

* Usar Ruby :)
* É permitido o uso de frameworks e _gems_, sem penalização
* A arquitetura e design do sistema devem ser documentadas em um arquivo README
* Deve ser usado GIT para versionamento

### Envio

Nos comunique através de e-mail, com um link para um repositório público no GitHub.

### Aviso

Ao completar o desafio não implica em nenhum vínculo nem obrigação da 4Asset com você. Todo o código criado será descartado. 
Esse teste usa elementos reais de necessidades da 4Asset apenas como uma maneira de avaliarmos sua aptidão para o cargo.

### Final notes

Valorizamos muito a sua capacidade de nos surpreender!

Boa sorte :)
