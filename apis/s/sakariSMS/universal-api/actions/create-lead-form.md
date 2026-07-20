# Sakari SMS: Create Lead Form

Creates a new lead form in Sakari SMS.

```
POST https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-lead-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-lead-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-lead-form', {
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
| `template` | string | no | Id of the form template you wish to clone |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "2026-05-07T12:00:00.000Z",
      "conversions": 1,
      "created": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
        }
      },
      "id": "string",
      "impressions": 1,
      "name": "Ava Chen",
      "updated": {
        "at": "2026-05-07T12:00:00.000Z",
        "by": {
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "name": "Ava Chen",
          "source": "string",
          "subSource": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | date |  |
| `conversions` | number |  |
| `created` | object |  |
| `created.at` | date |  |
| `created.by` | object |  |
| `created.by.email` | string |  |
| `created.by.firstName` | string |  |
| `created.by.id` | string |  |
| `created.by.lastName` | string |  |
| `created.by.name` | string |  |
| `created.by.source` | string |  |
| `created.by.subSource` | string |  |
| `id` | string |  |
| `impressions` | number |  |
| `name` | string |  |
| `updated` | object |  |
| `updated.at` | date |  |
| `updated.by` | object |  |
| `updated.by.email` | string |  |
| `updated.by.firstName` | string |  |
| `updated.by.id` | string |  |
| `updated.by.lastName` | string |  |
| `updated.by.name` | string |  |
| `updated.by.source` | string |  |
| `updated.by.subSource` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `POST /v1/accounts/:accountId/forms` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-form.md) for the provider-specific parameters and requirements.

