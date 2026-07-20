# Zixflow: Create List Entry

Creates a new list entry in Zixflow.

```
POST https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-list-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/create-list-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | List identifier. |
| `recordId` | string | yes | Record identifier to add to the list. |
| `data` | object | no | Additional list-entry data payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created list-entry payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the list-entry create request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `POST /list-entries/:listId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list-entry.md) for the provider-specific parameters and requirements.

