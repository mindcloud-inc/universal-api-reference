# Brasil API: List National Holidays

Retrieves Brazilian national holidays from Brasil API by year.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-national-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-national-holidays?connectionId=$CONNECTION_ID&ano=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ano": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-national-holidays?${params}`, {
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
| `ano` | string | yes | The year to list national holidays for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "fullName": "Ava Chen",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `fullName` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /feriados/v1/{ano}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-national-holidays.md) for the provider-specific parameters and requirements.

