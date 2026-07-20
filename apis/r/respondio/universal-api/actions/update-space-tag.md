# respond.io: Update Space Tag

Updates an existing space tag in respond.io.

```
PUT https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-space-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-space-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currentName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/update-space-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currentName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `colorCode` | string | no | Hex color code for the tag. |
| `currentName` | string | yes | Current space tag name. |
| `description` | string | no | Space tag description. |
| `emoji` | string | no | Emoji for the tag. |
| `name` | string | no | New space tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | object |  |

## Native endpoint

Through the native respond.io API, this operation is `PUT /space/tag` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space-tag.md) for the provider-specific parameters and requirements.

