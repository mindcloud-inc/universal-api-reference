# Maildrip: Update metadata attributes for multiple contacts



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-metadata-attributes-for-multiple-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-metadata-attributes-for-multiple-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIds[]": [
    "string"
  ],
  "attributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/update-metadata-attributes-for-multiple-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIds[]": ["string"],
    "attributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds[]` | array<string> | yes | Array of contact IDs to update (max 100) Accepts multiple values as an array. |
| `attributes` | object | yes | Object with attribute key-value pairs to update (max 10 attributes). Keys must be alphanumeric with underscores/hyphens (max 50 chars). Values must be primitives (max 500 chars). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `PUT /api/v1/contacts/bulk-attributes` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-metadata-attributes-for-multiple-contacts.md) for the provider-specific parameters and requirements.

