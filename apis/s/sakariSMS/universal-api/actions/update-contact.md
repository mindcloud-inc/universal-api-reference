# Sakari SMS: Update Contact

Updates an existing contact in Sakari SMS.

```
PUT https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `mobile` | object | no |  |
| `mobile.number` | string | no |  |
| `mobile.country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activecampaign": {
        "id": 1
      },
      "attributes": {},
      "blocked": "2026-05-07T12:00:00.000Z",
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
      "email": "ava@example.com",
      "error": {
        "code": "string",
        "description": "string"
      },
      "firstName": "Ava",
      "hubspot": {
        "id": 1
      },
      "id": "string",
      "lastName": "Chen",
      "lists": {
        "lists": [
          {
            "doubleOptIn": {
              "enabled": true,
              "prompt": "string"
            },
            "filter": {
              "attributes": [
                {}
              ],
              "blocked": true,
              "invalid": true,
              "list": "string",
              "optIn": true,
              "q": "string",
              "unblocked": true,
              "valid": true
            },
            "id": "string",
            "keyword": "string",
            "name": "Ava Chen",
            "optIn": "2026-05-07T12:00:00.000Z",
            "optInConfirmation": "string",
            "optOut": "2026-05-07T12:00:00.000Z",
            "source": {
              "id": "string",
              "integration": "string",
              "lastSynced": "string"
            }
          }
        ]
      },
      "mobile": {
        "country": "string",
        "lineType": "string",
        "number": "string",
        "valid": true,
        "verified": "2026-05-07T12:00:00.000Z"
      },
      "optIn": "2026-05-07T12:00:00.000Z",
      "pipedrive": {
        "id": 1
      },
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
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activecampaign` | object |  |
| `activecampaign.id` | number |  |
| `attributes` | object |  |
| `blocked` | date |  |
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
| `email` | string |  |
| `error` | object |  |
| `error.code` | string |  |
| `error.description` | string |  |
| `firstName` | string |  |
| `hubspot` | object |  |
| `hubspot.id` | number |  |
| `id` | string |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `lists.lists[].doubleOptIn` | object |  |
| `lists.lists[].doubleOptIn.enabled` | boolean |  |
| `lists.lists[].doubleOptIn.prompt` | string |  |
| `lists.lists[].filter` | object |  |
| `lists.lists[].filter.attributes` | array<object> |  |
| `lists.lists[].filter.blocked` | boolean |  |
| `lists.lists[].filter.invalid` | boolean |  |
| `lists.lists[].filter.list` | string |  |
| `lists.lists[].filter.optIn` | boolean |  |
| `lists.lists[].filter.q` | string |  |
| `lists.lists[].filter.unblocked` | boolean |  |
| `lists.lists[].filter.valid` | boolean |  |
| `lists.lists[].id` | string |  |
| `lists.lists[].keyword` | string |  |
| `lists.lists[].name` | string |  |
| `lists.lists[].optIn` | date |  |
| `lists.lists[].optInConfirmation` | string |  |
| `lists.lists[].optOut` | date |  |
| `lists.lists[].source` | object |  |
| `lists.lists[].source.id` | string |  |
| `lists.lists[].source.integration` | string |  |
| `lists.lists[].source.lastSynced` | string |  |
| `mobile` | object |  |
| `mobile.country` | string |  |
| `mobile.lineType` | string |  |
| `mobile.number` | string |  |
| `mobile.valid` | boolean |  |
| `mobile.verified` | date |  |
| `optIn` | date |  |
| `pipedrive` | object |  |
| `pipedrive.id` | number |  |
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
| `valid` | boolean |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `PUT /v1/accounts/:accountId/contacts/:contactId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

