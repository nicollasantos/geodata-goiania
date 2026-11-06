# geodata-goiania

Contornos de bairros de Goiânia e Aparecida de Goiânia (GO) em GeoJSON, coordenadas geográficas WGS84.

`bairros-goiania-aparecida.geojson`: um polígono por bairro, com as propriedades

| Propriedade | Conteúdo |
|---|---|
| `chave` | identificador do bairro: `cidade|tipo|nome` normalizado (sem acento, maiúsculo, tipo abreviado), ex. `GYN|S|SUL` |
| `nome` | nome do bairro para exibição, ex. `Setor Sul` |
| `cidade` | `Goiânia` ou `Aparecida de Goiânia` |

## Fontes

- Goiânia: dados abertos da Prefeitura de Goiânia (SEDETEC), camada de bairros, reprojetada de SIRGAS 2000 / UTM 22S.
- Aparecida de Goiânia: shapefile de bairros publicado em forest-gis.com.

Geometria simplificada com mapshaper para uso em mapas de região (ex.: Metabase).

`depara-bairros-cadastro.csv`: grafias de bairro encontradas em cadastro (cidade `GYN`/`APG` + nome em maiúsculo) ligadas à `chave` e ao `nome` do GeoJSON. A coluna `como` diz se a ligação foi exata, só pelo nome, aproximada ou manual.
