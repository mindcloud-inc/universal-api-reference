# Dripcel: Remove Tags from Contact

Updates a contact to remove tags in Dripcel.

```
PUT https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/remove-tags-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/remove-tags-from-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cell": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/remove-tags-from-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cell": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cell` | string | yes |  |
| `tagIds[]` | array<string> | no | The tag IDs to remove from the contact. |
| `tags[]` | array<string> | no | The tag names to remove from the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "acknowledged": true,
        "matchedCount": 1,
        "modifiedCount": 1,
        "upsertedCount": 1,
        "upsertedId": {}
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.acknowledged` | boolean |  |
| `data.matchedCount` | number |  |
| `data.modifiedCount` | number |  |
| `data.upsertedCount` | number |  |
| `data.upsertedId` | object |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `PUT /contacts/:cell/tag/remove` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tags-from-contact.md) for the provider-specific parameters and requirements.

