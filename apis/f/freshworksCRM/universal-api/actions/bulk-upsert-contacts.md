# Freshworks CRM: Bulk Upsert Contacts

Finds or creates multiple contacts in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-upsert-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-upsert-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/bulk-upsert-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes |  |
| `contacts[].data` | object | no |  |
| `contacts[].data.firstName` | string | no |  |
| `contacts[].data.lastName` | string | no |  |
| `contacts[].emails` | string | no |  |
| `contacts[].id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job_status_url": "https://example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job_status_url` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/contacts/bulk_upsert` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upsert-contacts.md) for the provider-specific parameters and requirements.

