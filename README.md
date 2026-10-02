# Geoportal — Pedro Juan Caballero · Ponta Porã

Geoportal bilíngue (português e espanhol) sobre a cidade-gêmea Pedro Juan Caballero (Paraguai) e Ponta Porã (Brasil), contado em três capítulos.

🔗 **Acesse ao vivo:** <https://mirianniz-debug.github.io/PedroJuanCaballero/>

## Capítulos

- **Cidade-gêmea** — a fronteira urbana (a "Linha") em destaque; área urbana oficial dos censos 2022 do INE (Paraguai) e do IBGE (Brasil); vias, áreas verdes, hidrografia e equipamentos (OpenStreetMap); janelas sobre o mapa com os números dos dois lados e os costumes da fronteira; cortina para comparar fotos de satélite de 2007 a 2022 (Esri Wayback).
- **Crescimento** — linha do tempo da mancha urbana de 1985 a 2020 (MapBiomas Paraguay e MapBiomas Brasil), com gráfico de área por ano.
- **Memória e cultura** — lugares históricos, monumentos e parques com foto, fato e fonte.
- **Territórios** — os 6 distritos de Amambay (INE) e o município de Ponta Porã (IBGE).

As fontes e licenças de cada camada estão no botão **Fonte de dados** do próprio site.

## Como acrescentar lugares na aba Memória

Os lugares vêm da planilha `data/memoria/lugares.csv` (abre no Excel, Google Planilhas ou QGIS) e as fotos ficam em `data/memoria/fotos/`. O passo a passo está em [`data/memoria/COMO-EDITAR.txt`](data/memoria/COMO-EDITAR.txt).

## Tecnologias

- Leaflet.js e HTML/CSS/JavaScript puro (sem build nem dependências)
- Dados preparados no QGIS e com Python (GDAL, Shapely)

## Como visualizar localmente

Sirva a pasta com um servidor estático simples (abrir o `index.html` direto não carrega os dados):

```bash
python3 -m http.server 8000
```

Depois acesse `http://localhost:8000` no navegador.

## Incorporando o geoportal em outro site (iframe)

O `index.html` é responsivo, mas isso só funciona se o `<iframe>` que o incorpora também for responsivo. Use sempre largura em porcentagem, nunca um valor fixo em pixels:

```html
<iframe src="https://mirianniz-debug.github.io/PedroJuanCaballero/" style="width:100%; border:0;" height="600" loading="lazy"></iframe>
```

## Licença

Código, textos e cartografia: todos os direitos reservados a Mirian Niz. Dados e fotos de terceiros mantêm suas próprias licenças. Ver [LICENSE](LICENSE).
