# MedClin

Para criar o projeto basta baixar o repositório com  clone, ativar o .venv com o ```venv\Scripts\Activate```.
Pode ser necessário instalar o django ```pip install django```. É importante rodar o servidor ``` python manage.py runserver ```.

A estrutura do projeto é:

```
meu_projeto/
│
├── manage.py
├── requirements.txt
│
├── config/                  # Configuração do projeto (core)
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── apps/                    # Camada de negócio
│   ├── acesso/
│   ├── cadastros/
│   ├── atendimento/
│   ├── prontuario/
│   ├── farmacia/
│   └── financeiro/
│
├── core/                    # Código compartilhado (regras comuns)
│   ├── models/
│   ├── services/
│   ├── utils/
│   └── validators/
│
├── templates/               # Camada de apresentação (HTML global)
│   └── base.html
│
├── static/                  # CSS, JS, imagens
│   ├── css/
│   ├── js/
│   └── img/
│
├── media/                   # Uploads (arquivos do usuário)
│
└── db.sql                   # Banco
```

Dentro da pasta de atendimento, por exemplo, podemos ter algo assim:
```
atendimento/
├── models.py                # estrutura dos dados
├── views.py
├── urls.py                  # apenas para manipular, sem regras complexas
├── admin.py
```
