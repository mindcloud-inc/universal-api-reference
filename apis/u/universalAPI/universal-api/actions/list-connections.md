# Universal API: List Connections

Retrieves a list of connections from Universal API.

```
GET https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-connections?${params}`, {
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
      "id": "string",
      "serviceId": "string",
      "status": "string",
      "universalApi": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `serviceId` | string |  |
| `status` | string |  |
| `universalApi` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `GET /api/connections` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connections.md) for the provider-specific parameters and requirements.

