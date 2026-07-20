# eGestor: Get Product

Retrieves details for a product from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-product?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "codigo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/get-product?${params}`, {
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
| `codigo` | number | yes | Código do produto. Example: `1`. |

## Response

```json
{
  "success": true,
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
      "excecaoIPI": "string",
      "margemLucro": 1,
      "ncm": "string",
      "origemFiscal": 1,
      "pesoBruto": "string",
      "pesoLiquido": "string",
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anotacoesInternas` | string |  |
| `anotacoesNFE` | string |  |
| `codCategoria` | number |  |
| `codigo` | number |  |
| `codigoCEST` | string |  |
| `codigoGrupoTributos` | number |  |
| `codigoProprio` | string |  |
| `controlarEstoque` | boolean |  |
| `descricao` | string |  |
| `dtCad` | date |  |
| `estoque` | number |  |
| `estoqueMinimo` | number |  |
| `excecaoIPI` | string |  |
| `margemLucro` | number |  |
| `ncm` | string |  |
| `origemFiscal` | number |  |
| `pesoBruto` | string |  |
| `pesoLiquido` | string |  |
| `precoCusto` | number |  |
| `precoVenda` | number |  |
| `refEanGtin` | string |  |
| `tags[]` | string |  |
| `tipoProduto` | string |  |
| `unidadeTributada` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /produtos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

