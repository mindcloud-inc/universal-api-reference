# eGestor: Update Service

Updates an existing service in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": "1",
  "descricao": "MindCloud Stage3 Service Updated 20260401"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/update-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": "1",
    "descricao": "MindCloud Stage3 Service Updated 20260401"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código do serviço. Example: `1`. |
| `descricao` | string | yes | Descrição do serviço. Example: `MindCloud Stage3 Service Updated 20260401`. |
| `precoVenda` | number | no | Preço de venda. Example: `399`. |
| `codigoGrupoTributos` | number | no | Código do grupo de tributos vinculado. Example: `0`. |
| `itemListaServico` | string | no | Código do item da lista de serviço. Example: `1.03`. |
| `cnae` | string | no | Código CNAE. Example: `1234567`. |
| `codTributacaoMun` | string | no | Código de tributação municipal. Example: `112233`. |

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

Through the native eGestor API, this operation is `PUT /servicos/:codigo` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service.md) for the provider-specific parameters and requirements.

