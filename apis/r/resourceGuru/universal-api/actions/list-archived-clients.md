# Resource Guru: List Archived Clients

Retrieves archived clients from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-archived-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-archived-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-archived-clients?${params}`, {
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
      "color": "string",
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Archived client color. |
| `id` | number | Archived client ID. |
| `name` | string | Archived client name. |
| `url` | string | Archived client URL. |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /clients/archived` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-archived-clients.md) for the provider-specific parameters and requirements.

