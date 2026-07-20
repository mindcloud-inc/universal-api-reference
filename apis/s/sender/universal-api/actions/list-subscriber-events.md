# Sender: List Subscriber Events



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscriber-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscriber-events?connectionId=$CONNECTION_ID&subscriberKey=user%40example.com&actions=See%20notes%20for%20format" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberKey": "user@example.com",
  "actions": "See notes for format"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscriber-events?${params}`, {
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
| `subscriberKey` | string | yes | Subscriber email address, phone number, or ID. Example: `user@example.com`. |
| `actions` | string<string> | yes | JSON array string of one or more event action types: opened, bounced, clicked, unsubscribed, or got. Example: `See notes for format`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customEvents": [
        "string"
      ],
      "email": {
        "channelStatus": [
          "ava@example.com"
        ],
        "got": [
          "ava@example.com"
        ]
      },
      "emailCampaign": {
        "bounced": 1,
        "clickedCount": 1,
        "openedCount": 1,
        "sentCount": 1,
        "spamReported": 1,
        "unsubscribed": 1
      },
      "siteVisits": [
        "string"
      ],
      "sms": {
        "channelStatus": [
          "string"
        ]
      },
      "smsCampaign": {
        "clickedCount": 1,
        "deliveredCount": 1,
        "failedCount": 1,
        "sentCount": 1,
        "unsubscribed": 1
      },
      "store": [
        "string"
      ],
      "subscriberChanges": [
        "string"
      ],
      "temail": {
        "channelStatus": [
          "ava@example.com"
        ],
        "got": [
          "ava@example.com"
        ]
      },
      "tsms": {
        "channelStatus": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customEvents` | array |  |
| `email.channelStatus` | array |  |
| `email.got` | array |  |
| `emailCampaign.bounced` | number |  |
| `emailCampaign.clickedCount` | number |  |
| `emailCampaign.openedCount` | number |  |
| `emailCampaign.sentCount` | number |  |
| `emailCampaign.spamReported` | number |  |
| `emailCampaign.unsubscribed` | number |  |
| `siteVisits` | array |  |
| `sms.channelStatus` | array |  |
| `smsCampaign.clickedCount` | number |  |
| `smsCampaign.deliveredCount` | number |  |
| `smsCampaign.failedCount` | number |  |
| `smsCampaign.sentCount` | number |  |
| `smsCampaign.unsubscribed` | number |  |
| `store` | array |  |
| `subscriberChanges` | array |  |
| `temail.channelStatus` | array |  |
| `temail.got` | array |  |
| `tsms.channelStatus` | array |  |

## Native endpoint

Through the native Sender API, this operation is `GET /subscribers/:subscriberKey/events` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-events.md) for the provider-specific parameters and requirements.

