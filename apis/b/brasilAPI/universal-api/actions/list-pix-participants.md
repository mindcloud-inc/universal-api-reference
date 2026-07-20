# Brasil API: List PIX Participants

Retrieves PIX participants from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-pix-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-pix-participants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-pix-participants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "inicio_operacao": "string",
      "ispb": "string",
      "modalidade_participacao": "string",
      "nome": "string",
      "nome_reduzido": "string",
      "tipo_participacao": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inicio_operacao` | string |  |
| `ispb` | string |  |
| `modalidade_participacao` | string |  |
| `nome` | string |  |
| `nome_reduzido` | string |  |
| `tipo_participacao` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /pix/v1/participants` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pix-participants.md) for the provider-specific parameters and requirements.

