# Sequenzy: Add Tags (Bulk)

Adds tags to multiple subscribers in Sequenzy.

```
POST https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/add-tags-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/add-tags-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "tags": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/add-tags-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "tags": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address. |
| `tags` | list<string> | yes | Tag names to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {
        "created": true,
        "email": "ava@example.com",
        "id": "string",
        "tags": [
          "string"
        ]
      },
      "success": true,
      "tags": {
        "added": [
          "string"
        ],
        "alreadyPresent": [
          "string"
        ],
        "created": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber.created` | boolean |  |
| `subscriber.email` | string |  |
| `subscriber.id` | string |  |
| `subscriber.tags` | array<string> |  |
| `success` | boolean |  |
| `tags.added` | array<string> |  |
| `tags.alreadyPresent` | array<string> |  |
| `tags.created` | array<string> |  |

## Native endpoint

Through the native Sequenzy API, this operation is `POST /subscribers/tags/bulk` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tags-bulk.md) for the provider-specific parameters and requirements.

