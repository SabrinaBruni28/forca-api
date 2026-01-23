# 🎯 Forca API

API simples em **JSON** para um **jogo da forca**, que fornece **categorias** e **palavras/frases aleatórias** de acordo com o idioma selecionado.

A API é **estática**, hospedada no **GitHub Pages**, ideal para projetos front-end, estudos e jogos educacionais.

---

## 🌐 Base URL

```
https://sabrinabruni28.github.io/forca-api/
```

---

## 🌍 Idiomas disponíveis

Estrutura da API:

```
/forca-api
├── index.json
├── portugues
│   ├── index.json
│   ├── animais.json
│   ├── frutas.json
│   ├── cores.json
│   └── ...
├── ingles
│   ├── index.json
│   ├── animals.json
│   ├── fruits.json
│   ├── colors.json
│   └── ...
```

---

## 📌 Lista de idiomas

Endpoint:

```
GET /index.json
```

Exemplo de resposta:

```json
{
  "linguagens": [
    { "key": "portugues", "name": "Português" },
    { "key": "ingles", "name": "Inglês" }
  ]
}
```

---

## 📂 Categorias por idioma

Endpoint:

```
GET /{idioma}/index.json
```

Exemplo:

```json
{
  "categorias": [
    {
      "key": "animais",
      "name": "Animais",
      "file": "animais.json"
    },
    {
      "key": "frutas",
      "name": "Frutas",
      "file": "frutas.json"
    }
  ]
}
```

---

## 🧠 Palavras por categoria

Endpoint:

```
GET /{idioma}/{categoria}.json
```

Exemplo:

```json
{
  "categoria": "Animais",
  "palavras": [
    "Cachorro",
    "Gato",
    "Elefante"
  ]
}
```

---

## 📄 Licença

Uso livre para fins educacionais, estudos e projetos pessoais.
