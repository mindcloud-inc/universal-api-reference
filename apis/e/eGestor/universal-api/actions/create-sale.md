# eGestor: Create Sale

Creates a new sale in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-sale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codContato": "3",
  "codVendedor": "1",
  "dtVenda": "2026-04-01",
  "situacao": "50",
  "produtos[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-sale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codContato": "3",
    "codVendedor": "1",
    "dtVenda": "2026-04-01",
    "situacao": "50",
    "produtos[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codContato` | number | yes | Código do contato cliente da venda. Example: `3`. |
| `dtVenda` | string | yes | Data da venda no formato YYYY-MM-DD. Example: `2026-04-01`. |
| `dtEntrega` | string | no | Data de entrega no formato YYYY-MM-DD. Example: `2026-04-02`. |
| `situacao` | list | yes | Situação da venda, como orçamento ou venda efetivada. One of: `10`, `50`. Example: `50`. |
| `valorFrete` | number | no | Valor do frete da venda. Example: `5.5`. |
| `valorDesc` | number | no | Valor do desconto da venda. Example: `0`. |
| `clienteFinal` | boolean | no | Define se o contato é cliente final. Example: `true`. |
| `produtos[]` | array<object> | yes | Lista de produtos da venda. Example: `[object Object]`. |
| `financeiros[]` | array<object> | no | Lista de recebimentos financeiros da venda. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codVendedor` | number | yes | Código do vendedor da venda. Example: `1`. |
| `tags[]` | array<string> | no | Tags da venda. Example: `VENDA_VIA_API`. |
| `valorDespesasAcessorias` | number | no | Valor das despesas acessórias da venda. Example: `0`. |
| `enderecoEntrega` | number | no | Código do endereço de entrega associado ao contato. Example: `1`. |
| `situacaoOS` | string | no | Situação da ordem de serviço quando aplicável. Example: `Em espera`. |
| `customizado` | object | no | Objeto com campos personalizados da venda. Example: `[object Object]`. |
| `despesas[]` | array<object> | no | Lista de despesas associadas à venda. Example: `[object Object]`. |

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
| `codVendedor` | number | Seller code linked to the created sale. |
| `dtVenda` | date | Sale date. |
| `valorTotal` | number | Total sale amount. |

## Native endpoint

Through the native eGestor API, this operation is `POST /vendas` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sale.md) for the provider-specific parameters and requirements.

