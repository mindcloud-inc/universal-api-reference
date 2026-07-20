# Sakari SMS: List Contacts

Retrieves account contacts from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastName` | string | no | Filter by last name or part of |
| `mobile` | string | no | Filter by mobile or part of |
| `email` | string | no | Filter by email or part of |
| `tags` | string | no | Filter by tag(s) |
| `tags` | string | no | Filter by tag(s) |

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

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/contacts` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

