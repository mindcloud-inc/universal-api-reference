# Routee: Retrieve details for a bulk send out - campaign

Retrieves details for a bulk send out - campaign from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-for-a-bulk-send-out-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-for-a-bulk-send-out-campaign?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-details-for-a-bulk-send-out-campaign?${params}`, {
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
| `trackingId` | string | yes | The tracking id of the campaign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "campaignName": "Ava Chen",
      "contacts": [
        [
          "string"
        ]
      ],
      "cost": 1,
      "createdAt": "string",
      "endedAt": "string",
      "fallbackValues": {
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "flash": true,
      "from": "string",
      "groups": [
        [
          "string"
        ]
      ],
      "respectQuietHours": true,
      "scheduledDate": "string",
      "smsAnalysis": {
        "bodyAnalysis": {
          "characters": 1,
          "parts": 1,
          "unicode": true
        },
        "contacts": {},
        "numberOfRecipients": 1,
        "recipientCountries": {},
        "recipientsPerCountry": {
          "ES": 1,
          "GR": 1
        },
        "recipientsPerGroup": {
          "AMD Telecom": 1
        },
        "totalInGroups": 1
      },
      "state": "string",
      "statuses": {
        "Delivered": 1,
        "Failed": 1,
        "Queued": 1,
        "Sent": 1,
        "Undelivered": 1,
        "Unsent": 1
      },
      "to": [
        [
          "string"
        ]
      ],
      "totalMessages": 1,
      "trackingId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `campaignName` | string |  |
| `contacts[]` | array |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `endedAt` | string |  |
| `fallbackValues` | object |  |
| `fallbackValues.firstName` | string |  |
| `fallbackValues.lastName` | string |  |
| `flash` | boolean |  |
| `from` | string |  |
| `groups[]` | array<string> |  |
| `respectQuietHours` | boolean |  |
| `scheduledDate` | string |  |
| `smsAnalysis` | object |  |
| `smsAnalysis.bodyAnalysis` | object |  |
| `smsAnalysis.bodyAnalysis.characters` | number |  |
| `smsAnalysis.bodyAnalysis.parts` | number |  |
| `smsAnalysis.bodyAnalysis.unicode` | boolean |  |
| `smsAnalysis.contacts` | object |  |
| `smsAnalysis.numberOfRecipients` | number |  |
| `smsAnalysis.recipientCountries` | object |  |
| `smsAnalysis.recipientsPerCountry` | object |  |
| `smsAnalysis.recipientsPerCountry.ES` | number |  |
| `smsAnalysis.recipientsPerCountry.GR` | number |  |
| `smsAnalysis.recipientsPerGroup` | object |  |
| `smsAnalysis.recipientsPerGroup.AMD Telecom` | number |  |
| `smsAnalysis.totalInGroups` | number |  |
| `state` | string |  |
| `statuses` | object |  |
| `statuses.Delivered` | number |  |
| `statuses.Failed` | number |  |
| `statuses.Queued` | number |  |
| `statuses.Sent` | number |  |
| `statuses.Undelivered` | number |  |
| `statuses.Unsent` | number |  |
| `to[]` | array |  |
| `totalMessages` | number |  |
| `trackingId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /campaigns/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-details-for-a-bulk-send-out-campaign.md) for the provider-specific parameters and requirements.

