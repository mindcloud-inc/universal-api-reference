# eGestor: Update Product

Updates an existing product in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": "1",
  "descricao": "MindCloud Stage3 Product Updated 20260401"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": "1",
    "descricao": "MindCloud Stage3 Product Updated 20260401"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código do produto. Example: `1`. |
| `descricao` | string | yes | Descrição do produto. Example: `MindCloud Stage3 Product Updated 20260401`. |
| `codigoProprio` | string | no | Código próprio do produto. Example: `MC-20260401-UPD`. |
| `estoque` | number | no | Quantidade em estoque. Example: `50`. |
| `controlarEstoque` | boolean | no | Define se o produto controla estoque. Example: `true`. |
| `precoCusto` | number | no | Preço de custo. Example: `5`. |
| `precoVenda` | number | no | Preço de venda. Example: `7.5`. |
| `origemFiscal` | number | no | Origem fiscal do produto. Example: `3`. |
| `unidadeTributada` | string | no | Unidade tributada. Example: `UN`. |
| `codigoGrupoTributos` | number | no | Código do grupo de tributos vinculado. Example: `0`. |

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

Through the native eGestor API, this operation is `PUT /produtos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

