# Brasil API: List IBGE Municipalities

Retrieves IBGE municipalities from Brasil API by state abbreviation.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-ibge-municipalities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-ibge-municipalities?connectionId=$CONNECTION_ID&siglaUF=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siglaUF": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-ibge-municipalities?${params}`, {
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
| `siglaUF` | string | yes | The IBGE state abbreviation. |
| `providers` | string | no | Optional comma-separated municipality data providers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo_ibge": "string",
      "nome": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo_ibge` | string |  |
| `nome` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /ibge/municipios/v1/{siglaUF}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ibge-municipalities.md) for the provider-specific parameters and requirements.

