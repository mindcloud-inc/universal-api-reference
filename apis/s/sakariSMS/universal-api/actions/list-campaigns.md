# Sakari SMS: List Campaigns

Retrieves account campaigns from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-campaigns?${params}`, {
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
| `name` | string | no | Filter by name or part of |

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
      "description": "string",
      "fieldMappings": {
        "fieldMappings": [
          {
            "attribute": "string",
            "column": "string",
            "mandatory": true
          }
        ]
      },
      "filters": {
        "attributes": {
          "attributes": [
            {
              "attribute": "string",
              "comparator": "string",
              "value": "string"
            }
          ]
        },
        "list": "string",
        "q": "string",
        "tags": {
          "tags": [
            {
              "tag": "string",
              "visible": true
            }
          ]
        }
      },
      "id": "string",
      "lastJob": {
        "created": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
        },
        "failures": 1,
        "id": "string",
        "invalid": [
          {}
        ],
        "price": 1,
        "status": "string",
        "submitted": 1
      },
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
      "nextExecution": "string",
      "paused": "string",
      "phoneNumberFilter": {
        "group": {
          "id": "string"
        }
      },
      "reporting": {
        "delay": "string",
        "destination": "string",
        "unit": "string",
        "when": "string"
      },
      "schedule": {
        "cron": "string",
        "frequency": "string",
        "timezone": "string"
      },
      "template": "string",
      "trigger": {
        "code": "string",
        "name": "Ava Chen"
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
| `description` | string |  |
| `fieldMappings` | array<object> |  |
| `fieldMappings.fieldMappings[].attribute` | string |  |
| `fieldMappings.fieldMappings[].column` | string |  |
| `fieldMappings.fieldMappings[].mandatory` | boolean |  |
| `filters` | object |  |
| `filters.attributes` | array<object> |  |
| `filters.attributes.attributes[].attribute` | string |  |
| `filters.attributes.attributes[].comparator` | string |  |
| `filters.attributes.attributes[].value` | string |  |
| `filters.list` | string |  |
| `filters.q` | string |  |
| `filters.tags` | array<object> |  |
| `filters.tags.tags[].tag` | string |  |
| `filters.tags.tags[].visible` | boolean |  |
| `id` | string |  |
| `lastJob` | object |  |
| `lastJob.created` | object |  |
| `lastJob.created.at` | date |  |
| `lastJob.created.by` | object |  |
| `lastJob.failures` | number |  |
| `lastJob.id` | string |  |
| `lastJob.invalid` | array<object> |  |
| `lastJob.price` | number |  |
| `lastJob.status` | string |  |
| `lastJob.submitted` | number |  |
| `media` | array<object> | List of media objects attached to message |
| `media.media[].filename` | string |  |
| `media.media[].name` | string |  |
| `media.media[].type` | string |  |
| `media.media[].url` | string |  |
| `name` | string |  |
| `nextExecution` | string |  |
| `paused` | string |  |
| `phoneNumberFilter` | object |  |
| `phoneNumberFilter.group` | object |  |
| `phoneNumberFilter.group.id` | string |  |
| `reporting` | object |  |
| `reporting.delay` | string |  |
| `reporting.destination` | string |  |
| `reporting.unit` | string |  |
| `reporting.when` | string |  |
| `schedule` | object |  |
| `schedule.cron` | string |  |
| `schedule.frequency` | string |  |
| `schedule.timezone` | string |  |
| `template` | string |  |
| `trigger` | object |  |
| `trigger.code` | string |  |
| `trigger.name` | string |  |
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

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/campaigns` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

