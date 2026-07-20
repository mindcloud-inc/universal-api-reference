# Apilio: List Boolean Variables



```
GET https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables?${params}`, {
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
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |
| `value` | boolean |  |

## Native endpoint

Through the native Apilio API, this operation is `GET /api/v1/boolean_variables` (base URL `https://api.apilio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boolean-variables.md) for the provider-specific parameters and requirements.

