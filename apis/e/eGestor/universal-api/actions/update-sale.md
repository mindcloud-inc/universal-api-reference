# eGestor: Update Sale

Updates an existing sale in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": "1",
  "situacao": "50"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-sale', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": "1",
    "situacao": "50"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código da venda. Example: `1`. |
| `situacao` | list | yes | Nova situação da venda. One of: `10`, `50`. Example: `50`. |
| `situacaoOS` | string | no | Nova situação da ordem de serviço. Example: `Entregue`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campoAdicional1` | string | no | Conteúdo do campo adicional 1. Example: `Garantia de 3 meses`. |
| `campoAdicional2` | string | no | Conteúdo do campo adicional 2. Example: `Produto novo`. |
| `campoAdicional3` | string | no | Conteúdo do campo adicional 3. Example: `Serial 12345`. |
| `campoAdicional4` | string | no | Conteúdo do campo adicional 4. Example: `Entrega prevista 10/10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "codVendedor": 1,
      "dtVenda": "2026-05-07T12:00:00.000Z",
      "valorTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo` | number | Internal sale code. |
| `codVendedor` | number | Seller code linked to the updated sale. |
| `dtVenda` | date | Sale date. |
| `valorTotal` | number | Total sale amount after the update. |

## Native endpoint

Through the native eGestor API, this operation is `PUT /vendas/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sale.md) for the provider-specific parameters and requirements.

