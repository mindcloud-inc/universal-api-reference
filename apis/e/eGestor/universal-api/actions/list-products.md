# eGestor: List Products

Retrieves a list of products from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filtro` | string | no | Busca a string informada nos campos código do produto, código próprio e nome do produto. Example: `MindCloud Stage3 Product 20260401`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `controlarEstoque` | list | no | Filtra por produtos que controlam ou não controlam estoque. Valores documentados: 0 ou 1. One of: `0`, `1`. Example: `1`. |
| `fields` | string | no | Campos a retornar separados por vírgula. Example: `codigo,descricao,precoVenda`. |
| `orderBy` | string | no | Ordenação da listagem no formato campo,direção. Example: `descricao,asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "anotacoesInternas": "string",
          "anotacoesNFE": "string",
          "codCategoria": 1,
          "codigo": 1,
          "codigoCEST": "string",
          "codigoGrupoTributos": 1,
          "codigoProprio": "string",
          "controlarEstoque": true,
          "descricao": "string",
          "dtCad": "2026-05-07T12:00:00.000Z",
          "estoque": 1,
          "estoqueMinimo": 1,
          "excecaoIPI": 1,
          "margemLucro": 1,
          "ncm": "string",
          "origemFiscal": 1,
          "pesoBruto": 1,
          "pesoLiquido": 1,
          "precoCusto": 1,
          "precoVenda": 1,
          "refEanGtin": "string",
          "tags": [
            "string"
          ],
          "tipoProduto": "string",
          "unidadeTributada": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].anotacoesInternas` | string |  |
| `data[].anotacoesNFE` | string |  |
| `data[].codCategoria` | number |  |
| `data[].codigo` | number |  |
| `data[].codigoCEST` | string |  |
| `data[].codigoGrupoTributos` | number |  |
| `data[].codigoProprio` | string |  |
| `data[].controlarEstoque` | boolean |  |
| `data[].descricao` | string |  |
| `data[].dtCad` | date |  |
| `data[].estoque` | number |  |
| `data[].estoqueMinimo` | number |  |
| `data[].excecaoIPI` | number |  |
| `data[].margemLucro` | number |  |
| `data[].ncm` | string |  |
| `data[].origemFiscal` | number |  |
| `data[].pesoBruto` | number |  |
| `data[].pesoLiquido` | number |  |
| `data[].precoCusto` | number |  |
| `data[].precoVenda` | number |  |
| `data[].refEanGtin` | string |  |
| `data[].tags[]` | string |  |
| `data[].tipoProduto` | string |  |
| `data[].unidadeTributada` | string |  |
| `data[].updatedAt` | date |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /produtos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

