# Sakari SMS: Create And Execute Campaign

Creates and launches a campaign in Sakari SMS.

```
POST https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-and-execute-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-and-execute-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "groupId": "string",
  "listId": "string",
  "message": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-and-execute-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "groupId": "string",
    "listId": "string",
    "message": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `groupId` | string | yes |  |
| `listId` | string | yes |  |
| `message` | object | yes |  |
| `message.message` | string | no |  |
| `message.media[]` | array<object> | no |  |
| `message.media.media[].url` | string | no |  |
| `message.media.media[].type` | string | no |  |
| `message.media.media[].name` | string | no |  |
| `message.media.media[].filename` | string | no |  |
| `sendAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "created": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
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
          "attributes": [
            {}
          ],
          "list": "string",
          "q": "string",
          "tags": [
            {}
          ]
        },
        "id": "string",
        "lastJob": {
          "created": {},
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
          "group": {}
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
          "by": {}
        }
      },
      "job": {
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `campaign.created` | object |  |
| `campaign.created.at` | date |  |
| `campaign.created.by` | object |  |
| `campaign.description` | string |  |
| `campaign.fieldMappings` | array<object> |  |
| `campaign.fieldMappings.fieldMappings[].attribute` | string |  |
| `campaign.fieldMappings.fieldMappings[].column` | string |  |
| `campaign.fieldMappings.fieldMappings[].mandatory` | boolean |  |
| `campaign.filters` | object |  |
| `campaign.filters.attributes` | array<object> |  |
| `campaign.filters.list` | string |  |
| `campaign.filters.q` | string |  |
| `campaign.filters.tags` | array<object> |  |
| `campaign.id` | string |  |
| `campaign.lastJob` | object |  |
| `campaign.lastJob.created` | object |  |
| `campaign.lastJob.failures` | number |  |
| `campaign.lastJob.id` | string |  |
| `campaign.lastJob.invalid` | array<object> |  |
| `campaign.lastJob.price` | number |  |
| `campaign.lastJob.status` | string |  |
| `campaign.lastJob.submitted` | number |  |
| `campaign.media` | array<object> | List of media objects attached to message |
| `campaign.media.media[].filename` | string |  |
| `campaign.media.media[].name` | string |  |
| `campaign.media.media[].type` | string |  |
| `campaign.media.media[].url` | string |  |
| `campaign.name` | string |  |
| `campaign.nextExecution` | string |  |
| `campaign.paused` | string |  |
| `campaign.phoneNumberFilter` | object |  |
| `campaign.phoneNumberFilter.group` | object |  |
| `campaign.reporting` | object |  |
| `campaign.reporting.delay` | string |  |
| `campaign.reporting.destination` | string |  |
| `campaign.reporting.unit` | string |  |
| `campaign.reporting.when` | string |  |
| `campaign.schedule` | object |  |
| `campaign.schedule.cron` | string |  |
| `campaign.schedule.frequency` | string |  |
| `campaign.schedule.timezone` | string |  |
| `campaign.template` | string |  |
| `campaign.trigger` | object |  |
| `campaign.trigger.code` | string |  |
| `campaign.trigger.name` | string |  |
| `campaign.updated` | object |  |
| `campaign.updated.at` | date |  |
| `campaign.updated.by` | object |  |
| `job` | object |  |
| `job.created` | object |  |
| `job.created.at` | date |  |
| `job.created.by` | object |  |
| `job.failures` | number |  |
| `job.id` | string |  |
| `job.invalid` | array<object> |  |
| `job.price` | number |  |
| `job.status` | string |  |
| `job.submitted` | number |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `POST /v1/accounts/:accountId/quickcampaigns` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-and-execute-campaign.md) for the provider-specific parameters and requirements.

