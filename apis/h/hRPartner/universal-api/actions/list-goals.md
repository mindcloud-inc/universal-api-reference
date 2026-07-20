# HR Partner: List Goals



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-goals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-goals?${params}`, {
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
      "currentValue": 1,
      "description": "string",
      "dueAt": "2026-05-07T12:00:00.000Z",
      "employee": {},
      "id": 1,
      "isActive": true,
      "isCompleted": true,
      "scope": "string",
      "targetValue": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentValue` | number |  |
| `description` | string |  |
| `dueAt` | date |  |
| `employee` | object |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isCompleted` | boolean |  |
| `scope` | string |  |
| `targetValue` | number |  |
| `type` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /goals` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-goals.md) for the provider-specific parameters and requirements.

