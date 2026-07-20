# Cliengo: Get Site Chatbot



```
GET https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-site-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliengo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-site-chatbot?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliengo/latest/actions/get-site-chatbot?${params}`, {
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
| `id` | string | yes | Identifier of the Cliengo site. |

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

Through the native Cliengo API, this operation is `GET /sites/:id/chatbot` (base URL `https://api.cliengo.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-chatbot.md) for the provider-specific parameters and requirements.

