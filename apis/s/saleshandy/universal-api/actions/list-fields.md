# Saleshandy: List Fields



```
GET https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saleshandy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-fields?connectionId=$CONNECTION_ID&systemFields=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "systemFields": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/list-fields?${params}`, {
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
| `systemFields` | boolean | yes | Whether to return Saleshandy system fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "payload": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `payload` | array<object> |  |

## Native endpoint

Through the native Saleshandy API, this operation is `GET /fields` (base URL `https://open-api.saleshandy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

