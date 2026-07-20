# Emelia: Get Campaign

Retrieves a campaign from Emelia by ID.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/get-campaign?${params}`, {
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
| `id` | string | yes | Campaign identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "campaign": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "estimatedEnd": "2026-05-07T12:00:00.000Z",
          "lastRefreshed": {},
          "name": "Ava Chen",
          "plannedStart": {},
          "provider": "string",
          "recipients": {
            "processing": true,
            "totalCount": 1
          },
          "schedule": {
            "bcc": {},
            "blacklistUnsub": true,
            "dailyContact": 1,
            "dailyLimit": 1,
            "days": [
              1
            ],
            "end": "string",
            "eventToStopMails": [
              "string"
            ],
            "maxInterval": 1,
            "minInterval": 1,
            "start": "string",
            "timeZone": "string",
            "trackLinks": true,
            "trackOpens": true
          },
          "startAt": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "useManyProviders": true
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
| `data.campaign.createdAt` | date |  |
| `data.campaign.estimatedEnd` | date |  |
| `data.campaign.lastRefreshed` | object |  |
| `data.campaign.name` | string |  |
| `data.campaign.plannedStart` | object |  |
| `data.campaign.provider` | string |  |
| `data.campaign.recipients.processing` | boolean |  |
| `data.campaign.recipients.totalCount` | number |  |
| `data.campaign.schedule.bcc` | object |  |
| `data.campaign.schedule.blacklistUnsub` | boolean |  |
| `data.campaign.schedule.dailyContact` | number |  |
| `data.campaign.schedule.dailyLimit` | number |  |
| `data.campaign.schedule.days[]` | number |  |
| `data.campaign.schedule.end` | string |  |
| `data.campaign.schedule.eventToStopMails[]` | string |  |
| `data.campaign.schedule.maxInterval` | number |  |
| `data.campaign.schedule.minInterval` | number |  |
| `data.campaign.schedule.start` | string |  |
| `data.campaign.schedule.timeZone` | string |  |
| `data.campaign.schedule.trackLinks` | boolean |  |
| `data.campaign.schedule.trackOpens` | boolean |  |
| `data.campaign.startAt` | date |  |
| `data.campaign.status` | string |  |
| `data.campaign.useManyProviders` | boolean |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

