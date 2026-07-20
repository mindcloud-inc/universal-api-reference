# eGestor: Generate Sale NFe

Generates an NFe for a sale in eGestor.

```
PUT https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/generate-sale-n-fe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/generate-sale-n-fe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codigo": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/generate-sale-n-fe', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codigo": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codigo` | number | yes | Código da venda. Example: `1`. |
| `enviar` | boolean | no | Define se a nota deve ser enviada à SEFAZ. Example: `false`. |
| `contigOffline` | boolean | no | Define se a emissão será em contingência offline. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errMsg": "string",
      "errObs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errMsg` | string |  |
| `errObs` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /vendas/:codigo/gerarNfe` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-sale-n-fe.md) for the provider-specific parameters and requirements.

