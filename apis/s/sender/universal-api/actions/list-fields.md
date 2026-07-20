# Sender: List Fields



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-fields?${params}`, {
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
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "default": true,
      "defaultValue": "string",
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "position": 1,
      "show": true,
      "title": "string",
      "type": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | date |  |
| `default` | boolean |  |
| `defaultValue` | string |  |
| `id` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `position` | number |  |
| `show` | boolean |  |
| `title` | string |  |
| `type` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Sender API, this operation is `GET /fields` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

