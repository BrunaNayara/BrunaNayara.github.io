---
layout: post
title: Mandando emails com Python
---

> Esse texto é baseado na apresentação feita durante a Python Cerrado 2019, que aconteceu em Goiânia.


## Conteúdo
- [Usando a SMTPlib para enviar](#usando-a-smtplib-para-enviar)
- [Criando um template para o email](#criando-um-template-para-o-email)
- [Links](#links)


## [Usando a SMTPlib para enviar](#usando-a-smtplib-para-enviar)

Código básico para enviar um email usando a smtplib

```python
import smtplib

me = "eu@mail.com"
you = "voce@mail.com"
p = "senha"

server = smtplib.SMTP_SSL('smtp.gmail.com', 465)
server.login(me, p)
server.sendmail(me, you "this message is from python")
server.quit()
```

> Se você tiver autenticação de dois fatores, vai falhar.

Caso você esteja usando um email do gmail, pode seguir os passos a seguir para resolver.

1. Vai nas configurações da conta google
1. Clique em segurança
1. Vá em "Senhas de Aplicativos" na seção "Signing to google"
1. Gere um novo com as opções "Mail" e "Other"
1. Use a senha que foi gerada


## [Criando um template para o email](#criando-um-template-para-o-email)

Nesse exemplo, usamos um [template pronto](https://github.com/ohsik/Simple-Responsive-HTML-Email-Template).

> TO DO: colocar o resto da apresentação aqui.
Caso você tenha vindo aqui pra aprender mesmo, tem o código e a apresentação aqui embaixo

## [Links](#links)
[Apresentação](https://speakerdeck.com/brunamoreira/mandar-emails-com-python)

[Código](https://github.com/BrunaNayara/send-emails)

