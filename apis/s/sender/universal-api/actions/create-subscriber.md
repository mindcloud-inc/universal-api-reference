# Sender: Create Subscriber



```
POST https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/create-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The value must be a valid email address. Example: `user@example.com`. |
| `firstName` | string | no | Subscriber firstname. Example: `Jane`. |
| `lastName` | string | no | Subscriber lastname. Example: `Doe`. |
| `groups[]` | array<string> | no | Provide the new groups assigned to the subscriber. Example: `grp_123,grp_456`. |
| `fields` | object | no | Provide field key-value pairs for the subscriber. Example: `[object Object]`. |
| `phone` | string | no | Phone number must include the country code. Example: `+15551234567`. |
| `triggerAutomation` | boolean | no | Send false to avoid activating an automation. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {
          "default": true,
          "id": "string",
          "title": "string",
          "type": "string",
          "value": 1
        }
      ],
      "created": "string",
      "email": "ava@example.com",
      "emailCampaign": {
        "bounced": 1,
        "clickedCount": 1,
        "openedCount": 1,
        "sentCount": 1,
        "spamReported": 1,
        "unsubscribed": 1
      },
      "firstname": "Ava",
      "id": "string",
      "ipAddress": {},
      "lastname": "Chen",
      "location": {},
      "phone": "string",
      "phoneCountry": {
        "countryCode": "string",
        "phoneCode": 1
      },
      "smsCampaign": {
        "clickedCount": 1,
        "deliveredCount": 1,
        "failedCount": 1,
        "sentCount": 1,
        "unsubscribed": 1,
        "unsubscribedAt": {}
      },
      "status": {
        "email": "ava@example.com",
        "temail": "ava@example.com"
      },
      "subscriberTags": [
        {
          "id": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> |  |
| `columns[].default` | boolean |  |
| `columns[].id` | string |  |
| `columns[].title` | string |  |
| `columns[].type` | string |  |
| `columns[].value` | number |  |
| `created` | string |  |
| `email` | string |  |
| `emailCampaign` | object |  |
| `emailCampaign.bounced` | number |  |
| `emailCampaign.clickedCount` | number |  |
| `emailCampaign.openedCount` | number |  |
| `emailCampaign.sentCount` | number |  |
| `emailCampaign.spamReported` | number |  |
| `emailCampaign.unsubscribed` | number |  |
| `firstname` | string |  |
| `id` | string |  |
| `ipAddress` | object |  |
| `lastname` | string |  |
| `location` | object |  |
| `phone` | string |  |
| `phoneCountry` | object |  |
| `phoneCountry.countryCode` | string |  |
| `phoneCountry.phoneCode` | number |  |
| `smsCampaign` | object |  |
| `smsCampaign.clickedCount` | number |  |
| `smsCampaign.deliveredCount` | number |  |
| `smsCampaign.failedCount` | number |  |
| `smsCampaign.sentCount` | number |  |
| `smsCampaign.unsubscribed` | number |  |
| `smsCampaign.unsubscribedAt` | object |  |
| `status` | object |  |
| `status.email` | string |  |
| `status.temail` | string |  |
| `subscriberTags` | array<object> |  |
| `subscriberTags[].id` | string |  |
| `subscriberTags[].title` | string |  |

## Native endpoint

Through the native Sender API, this operation is `POST /subscribers` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscriber.md) for the provider-specific parameters and requirements.

