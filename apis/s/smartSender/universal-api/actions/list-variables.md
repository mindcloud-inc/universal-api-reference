# Smart Sender: List Variables

Retrieves project variables from Smart Sender.

```
GET https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-variables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/list-variables?${params}`, {
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
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | Variable content definition returned by Smart Sender. |
| `createdAt` | date | Variable creation timestamp. |
| `description` | string | Variable description. |
| `id` | number | Smart Sender variable ID. |
| `name` | string | Variable name. |
| `updatedAt` | date | Variable last update timestamp. |
| `value` | string | Current variable value. |

## Native endpoint

Through the native Smart Sender API, this operation is `GET /v1/variables` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-variables.md) for the provider-specific parameters and requirements.

