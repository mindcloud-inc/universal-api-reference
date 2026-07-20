# Cliengo: List Chatbots



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-chatbots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/list-chatbots?${params}`, {
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
      "aditionalQuestions": [
        {}
      ],
      "askDni": "string",
      "askEmail": "ava@example.com",
      "askTelephone": "string",
      "askTimeToCall": "string",
      "cliengoMeetings": true,
      "color": "string",
      "companyId": "string",
      "countryId": "string",
      "customMsgs": {},
      "defaultMsgs": {},
      "enabled": true,
      "globalTrigger": true,
      "labs": {},
      "language": "string",
      "name": "Ava Chen",
      "saluteTime": 1,
      "type": "string",
      "websiteId": "string",
      "widgetIcon": "string",
      "widgetStyle": "string",
      "windowTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aditionalQuestions` | array<object> |  |
| `askDni` | string |  |
| `askEmail` | string |  |
| `askTelephone` | string |  |
| `askTimeToCall` | string |  |
| `cliengoMeetings` | boolean |  |
| `color` | string |  |
| `companyId` | string |  |
| `countryId` | string |  |
| `customMsgs` | object |  |
| `defaultMsgs` | object |  |
| `enabled` | boolean |  |
| `globalTrigger` | boolean |  |
| `labs` | object |  |
| `language` | string |  |
| `name` | string |  |
| `saluteTime` | number |  |
| `type` | string |  |
| `websiteId` | string |  |
| `widgetIcon` | string |  |
| `widgetStyle` | string |  |
| `windowTitle` | string |  |

## Native endpoint

Through the native Cliengo API, this operation is `GET /sites/chatbots` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chatbots.md) for the provider-specific parameters and requirements.

