# Sakari SMS: Update Template

Updates an existing template in Sakari SMS.

```
PUT https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `name` | string | no |  |
| `template` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "media": {
        "media": [
          {
            "filename": "Ava Chen",
            "name": "Ava Chen",
            "type": "string",
            "url": "https://example.com"
          }
        ]
      },
      "name": "Ava Chen",
      "template": "string",
      "type": "string",
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
| `media` | array<object> | List of media objects attached to message |
| `media.media[].filename` | string |  |
| `media.media[].name` | string |  |
| `media.media[].type` | string |  |
| `media.media[].url` | string |  |
| `name` | string |  |
| `template` | string |  |
| `type` | string |  |
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

Through the native Sakari SMS API, this operation is `PUT /v1/accounts/:accountId/templates/:templateId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

