# eGestor: Create Purchase

Creates a new purchase in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-purchase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codContato": "2",
  "dtCompra": "2026-04-01",
  "situacao": "10",
  "atualizarPrecoVenda": "false",
  "produtos[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-purchase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codContato": "2",
    "dtCompra": "2026-04-01",
    "situacao": "10",
    "atualizarPrecoVenda": "false",
    "produtos[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codContato` | number | yes | Código do fornecedor da compra. Example: `2`. |
| `numNota` | string | no | Número do documento fiscal. Example: `775`. |
| `dtCompra` | string | yes | Data da realização da compra no formato YYYY-MM-DD. Example: `2026-04-01`. |
| `dtEntrega` | string | no | Data da entrega no formato YYYY-MM-DD. Example: `2026-04-01`. |
| `situacao` | number | yes | Situação da compra. Use 10 para orçamento ou 50 para compra efetivada. One of: `10`, `50`. Example: `10`. |
| `atualizarPrecoVenda` | boolean | yes | Define se o preço de venda será atualizado. Example: `false`. |
| `produtos[]` | array<object> | yes | Lista de itens da compra. Cada item deve incluir codProduto, custoBruto, quant, vDesc, valorIPI e valorST. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `financeiros[]` | array<object> | no | Lista de lançamentos financeiros quando aplicável. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codContato": 1,
      "codigo": 1,
      "dtCompra": "2026-05-07T12:00:00.000Z",
      "nomeContato": "string",
      "valorTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codContato` | number |  |
| `codigo` | number |  |
| `dtCompra` | date |  |
| `nomeContato` | string |  |
| `valorTotal` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /compras` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase.md) for the provider-specific parameters and requirements.

