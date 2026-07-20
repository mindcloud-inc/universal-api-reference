# TouchBasePro: Get Message

Retrieves a message from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "canBeResent": true,
      "clicks": [
        [
          {}
        ]
      ],
      "group": "string",
      "message": {
        "attachments": [
          [
            {}
          ]
        ],
        "bcc": [
          [
            "string"
          ]
        ],
        "body": {
          "html": "string",
          "text": "string"
        },
        "cc": [
          [
            "string"
          ]
        ],
        "from": "string",
        "replyTo": "string",
        "subject": "string",
        "to": [
          [
            "string"
          ]
        ]
      },
      "messageId": "string",
      "opens": [
        [
          {}
        ]
      ],
      "recipient": "string",
      "sentAt": "string",
      "smartEmailId": "ava@example.com",
      "status": "string",
      "totalClicks": 1,
      "totalOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBeResent` | boolean |  |
| `clicks[]` | array<object> |  |
| `clicks[].date` | string |  |
| `clicks[].emailAddress` | string |  |
| `clicks[].geolocation.city` | string |  |
| `clicks[].geolocation.countryCode` | string |  |
| `clicks[].geolocation.countryName` | string |  |
| `clicks[].geolocation.latitude` | number |  |
| `clicks[].geolocation.longitude` | number |  |
| `clicks[].geolocation.region` | string |  |
| `clicks[].ipAddress` | string |  |
| `clicks[].url` | string |  |
| `group` | string |  |
| `message.attachments[]` | array<object> |  |
| `message.attachments[].content` | string |  |
| `message.attachments[].name` | string |  |
| `message.attachments[].type` | string |  |
| `message.bcc[]` | array<string> |  |
| `message.body.html` | string |  |
| `message.body.text` | string |  |
| `message.cc[]` | array<string> |  |
| `message.from` | string |  |
| `message.replyTo` | string |  |
| `message.subject` | string |  |
| `message.to[]` | array<string> |  |
| `messageId` | string |  |
| `opens[]` | array<object> |  |
| `opens[].date` | string |  |
| `opens[].emailAddress` | string |  |
| `opens[].geolocation.city` | string |  |
| `opens[].geolocation.countryCode` | string |  |
| `opens[].geolocation.countryName` | string |  |
| `opens[].geolocation.latitude` | number |  |
| `opens[].geolocation.longitude` | number |  |
| `opens[].geolocation.region` | string |  |
| `opens[].ipAddress` | string |  |
| `opens[].mailClient.name` | string |  |
| `opens[].mailClient.version` | string |  |
| `recipient` | string |  |
| `sentAt` | string |  |
| `smartEmailId` | string |  |
| `status` | string |  |
| `totalClicks` | number |  |
| `totalOpens` | number |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/transactional/messages/{messageID}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

