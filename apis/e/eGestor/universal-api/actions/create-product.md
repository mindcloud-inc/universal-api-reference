# eGestor: Create Product

Creates a new product in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "descricao": "MindCloud Stage3 Product 20260401"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "descricao": "MindCloud Stage3 Product 20260401"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `descricao` | string | yes | Descrição do produto. Example: `MindCloud Stage3 Product 20260401`. |
| `codigoProprio` | string | no | Código próprio do produto. Example: `MC-20260401`. |
| `estoque` | number | no | Quantidade em estoque. Example: `100`. |
| `estoqueMinimo` | number | no | Estoque mínimo. Example: `0`. |
| `controlarEstoque` | boolean | no | Define se o produto controla estoque. Example: `true`. |
| `margemLucro` | number | no | Margem de lucro. Example: `0`. |
| `precoCusto` | number | no | Preço de custo. Example: `5`. |
| `precoVenda` | number | no | Preço de venda. Example: `10.37`. |
| `origemFiscal` | number | no | Origem fiscal do produto. Example: `0`. |
| `unidadeTributada` | string | no | Unidade tributada. Example: `UN`. |
| `codigoGrupoTributos` | number | no | Código do grupo de tributos vinculado. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<string> | no | Lista de tags do produto. Example: `exemplo,modelo`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "descricao": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo` | number |  |
| `descricao` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /produtos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

