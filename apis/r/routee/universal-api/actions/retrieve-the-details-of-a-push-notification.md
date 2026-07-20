# Routee: Retrieve the details of a Push Notification

Retrieves the details of a push notification from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-details-of-a-push-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-details-of-a-push-notification?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-details-of-a-push-notification?${params}`, {
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
| `trackingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "forceLocale": "string",
        "text": {
          "en": "string"
        },
        "title": {
          "en": "string"
        }
      },
      "callbackUrl": "https://example.com",
      "config": {
        "localizedText": "string",
        "localizedTitle": "string",
        "ttl": 1,
        "type": "string"
      },
      "createdAt": "string",
      "data": {
        "key1": "string",
        "key2": "string",
        "key3": "string",
        "key4": "string"
      },
      "deviceToken": {
        "token": "string",
        "type": "string"
      },
      "imageUrl": "https://example.com",
      "implementationId": "string",
      "owner": {
        "accountId": "string",
        "applicationId": "string"
      },
      "price": {
        "cost": 1,
        "currency": "string"
      },
      "serviceMessageId": "string",
      "statuses": [
        [
          {}
        ]
      ],
      "statusInfo": {
        "date": "string",
        "status": "string"
      },
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | object |  |
| `body.forceLocale` | string |  |
| `body.text` | object |  |
| `body.text.en` | string |  |
| `body.title` | object |  |
| `body.title.en` | string |  |
| `callbackUrl` | string |  |
| `config` | object |  |
| `config.localizedText` | string |  |
| `config.localizedTitle` | string |  |
| `config.ttl` | number |  |
| `config.type` | string |  |
| `createdAt` | string |  |
| `data` | object |  |
| `data.key1` | string |  |
| `data.key2` | string |  |
| `data.key3` | string |  |
| `data.key4` | string |  |
| `deviceToken` | object |  |
| `deviceToken.token` | string |  |
| `deviceToken.type` | string |  |
| `imageUrl` | string |  |
| `implementationId` | string |  |
| `owner` | object |  |
| `owner.accountId` | string |  |
| `owner.applicationId` | string |  |
| `price` | object |  |
| `price.cost` | number |  |
| `price.currency` | string |  |
| `serviceMessageId` | string |  |
| `statuses[]` | array<object> |  |
| `statuses[].date` | string |  |
| `statuses[].status` | string |  |
| `statusInfo` | object |  |
| `statusInfo.date` | string |  |
| `statusInfo.status` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /push-notifications/messages/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-the-details-of-a-push-notification.md) for the provider-specific parameters and requirements.

