# Geoportal — Pedro Juan Caballero (Paraguai)

Geoportal interativo com informações territoriais do município de Pedro Juan Caballero, Paraguai.

🔗 **Acesse ao vivo:** https://mirianniz-debug.github.io/PedroJuanCaballero/

👤 **Parte do portfólio de:** https://mirianniz-debug.github.io/Portfolio/

## Sobre

Mapa web para consulta espacial de dados territoriais do município, com camadas organizadas na pasta `data/`.

## Tecnologias

- Leaflet.js
- QGIS (exportado via QGIS2Web)
- HTML/CSS/JavaScript puro (sem build/dependências)

## Como visualizar localmente

Não há dependências ou build — basta abrir `index.html` diretamente no navegador, ou servir a pasta com um servidor estático simples:

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000` no navegador.

## Incorporando o geoportal em outro site (iframe)

O `index.html` é responsivo, mas isso só funciona se o `<iframe>` que o incorpora também for responsivo. Use sempre largura em porcentagem, nunca um valor fixo em pixels:

```html
<iframe src="URL_DO_GEOPORTAL" style="width:100%; border:0;" height="600" loading="lazy"></iframe>
```

## Licença

Todos os direitos reservados. Ver [LICENSE](LICENSE).
