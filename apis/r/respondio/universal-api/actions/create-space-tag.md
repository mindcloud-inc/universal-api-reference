# respond.io: Create Space Tag

Creates a new space tag in respond.io.

```
POST https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-space-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-space-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-space-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `colorCode` | string | no | Hex color code for the tag. |
| `description` | string | no | Space tag description. |
| `emoji` | string | no | Emoji for the tag. |
| `name` | string | yes | Space tag name. |

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

Through the native respond.io API, this operation is `POST /space/tag` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-space-tag.md) for the provider-specific parameters and requirements.

