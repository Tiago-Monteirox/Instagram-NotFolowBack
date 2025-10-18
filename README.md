# 🌐 Projeto: Site Estático no Amazon S3

Este projeto demonstra como **hospedar um site estático (HTML + JavaScript)** diretamente na **AWS S3**, sem precisar de servidor.  
O código principal está concentrado em um único arquivo `index.html`, que contém tanto a estrutura visual quanto a lógica JavaScript para leitura e exibição de dados em formato JSON.

---

## 🚀 Funcionalidades

- Leitura de dados de um arquivo **JSON** via `fetch()`.
- Estrutura de repetição (`for`) para percorrer e exibir os dados na página.
- Deploy direto na **nuvem AWS S3** com **Static Website Hosting** habilitado.
- Projeto totalmente **serverless** (sem backend).

---

## 🧠 Lógica do Script

A lógica principal está dentro de um `for` que percorre os dados do JSON:
```js
for (let item of dados) {
  // Exibe cada item do JSON
  console.log(item.nome);
}
```

O script:

1. Faz uma requisição ao JSON usando `fetch()`;
    
2. Converte a resposta com `response.json()`;
    
3. Itera sobre cada objeto retornado;
    
4. Atualiza o conteúdo do HTML dinamicamente.
    

Tudo acontece **no navegador** — o S3 apenas entrega os arquivos.

---

## ☁️ Hospedagem

O projeto está hospedado no **Amazon S3** com o recurso **Static Website Hosting** ativado.  
Isso permite acessar o site diretamente via um endpoint público como:

```perl
http://nome-do-bucket.s3-website-us-east-2.amazonaws.com
```

## 📚 Aprendizados

- Conceito de **deploy estático** (sem servidor).
    
- Uso básico de **S3** e permissões com **Bucket Policy**.
    
- Estrutura de repetição em JavaScript para manipulação de dados.
    
- Integração entre **HTML + JS + JSON** no front-end.
    

---

## 💡 Como replicar

1. Crie um bucket no Amazon S3.
    
2. Desmarque “Block all public access”.
    
3. Habilite **Static website hosting** e defina o `index.html`.
    
4. Faça upload dos arquivos (`index.html`, `dados.json`, etc).
    
5. Aplique a seguinte política de leitura pública:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::SEU-BUCKET/*"
    }
  ]
}
```

## 🖼️ Demonstração

🔗[[http://not-follow-back.s3-website.us-east-2.amazonaws.com/]]

_(O link pode levar alguns segundos para carregar, dependendo da propagação da AWS.)_

---

## ✨ Autor

Tiago Monteiro e Silva**  
💼 Estudante de ADS  | Estagiário de tecnologia

📫 [LinkedIn](https://www.linkedin.com/in/tiago-monteiro-e-silva-798300241/) | [Instagram](https://www.instagram.com/tiagomonteiroxx/)
