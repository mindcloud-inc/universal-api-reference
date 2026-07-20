# SWELLEnterprise: Bulk Create Contacts

Creates multiple contacts in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/bulk-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/bulk-create-contacts" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/bulk-create-contacts', {
  method: 'POST',
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
| `contacts[]` | array<object> | yes | Array of contact objects to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created": [
          {}
        ],
        "failed": [
          {}
        ],
        "summary": {
          "created": 1,
          "failed": 1,
          "total": 1
        }
      },
      "message": "string",
      "meta": {
        "timestamp": "2026-05-07T12:00:00.000Z",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.created` | array<object> | Created contacts. |
| `data.failed` | array<object> | Contacts that failed to create. |
| `data.summary.created` | number | Total contacts created. |
| `data.summary.failed` | number | Total contacts that failed. |
| `data.summary.total` | number | Total contacts processed. |
| `message` | string | Success message. |
| `meta.timestamp` | date | Response timestamp. |
| `meta.version` | string | API version. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /crm/contacts/bulk` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-contacts.md) for the provider-specific parameters and requirements.

