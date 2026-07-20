# XenForo: Mark Forum Read

Marks a forum as read in XenForo.

```
PUT https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/mark-forum-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/mark-forum-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/mark-forum-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the forum to mark read. Example: `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | number | no | Unix timestamp to mark the forum read to. Defaults to current time when omitted. Example: `1713571200`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native XenForo API, this operation is `POST /forums/:id/mark-read` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-forum-read.md) for the provider-specific parameters and requirements.

