# Freshworks CRM: Bulk Assign Contact Owner

Updates contact owners in Freshworks CRM in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-assign-contact-owner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-assign-contact-owner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ownerId": 1,
  "selectedIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-assign-contact-owner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ownerId": 1,
    "selectedIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ownerId` | number | yes |  |
| `selectedIds[]` | array<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/contacts/bulk_assign_owner` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-assign-contact-owner.md) for the provider-specific parameters and requirements.

