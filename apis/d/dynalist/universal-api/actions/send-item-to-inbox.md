# Dynalist: Send Item To Inbox

Creates a new inbox item in Dynalist.

```
POST https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/send-item-to-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/send-item-to-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/send-item-to-inbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `index` | number | no | Inbox insertion index; use -1 for the end. Default: `-1`. |
| `content` | string | no | Inbox item content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | no | Optional inbox item note. |
| `checked` | boolean | no | Whether the inbox item is checked. |
| `checkbox` | boolean | no | Whether the inbox item has a checkbox. |
| `heading` | number | no | Heading level. |
| `color` | number | no | Dynalist color index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "file_id": "string",
      "index": 1,
      "node_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |
| `file_id` | string |  |
| `index` | number |  |
| `node_id` | string |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /inbox/add` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-item-to-inbox.md) for the provider-specific parameters and requirements.

