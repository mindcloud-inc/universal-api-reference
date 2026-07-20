# SMS Connexion: Get Report Message

Retrieves a single message report from SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-message?connectionId=$CONNECTION_ID&msgId=4c5a6d39-65e8-4f22-a9c6-c5d3cbc0f8fe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msgId": "4c5a6d39-65e8-4f22-a9c6-c5d3cbc0f8fe"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/get-report-message?${params}`, {
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
| `msgId` | string | yes | Message UUID. Example: `4c5a6d39-65e8-4f22-a9c6-c5d3cbc0f8fe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "cost": 1,
      "countryIso": "string",
      "createdAt": "string",
      "data": {},
      "from": "string",
      "inQuietHours": true,
      "length": 1,
      "msgId": "string",
      "parts": 1,
      "source": "string",
      "status": "string",
      "statusCode": 1,
      "text": "string",
      "textAnalysis": {},
      "to": "string",
      "unicode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `createdAt` | string |  |
| `data` | object |  |
| `from` | string |  |
| `inQuietHours` | boolean |  |
| `length` | number |  |
| `msgId` | string |  |
| `parts` | number |  |
| `source` | string |  |
| `status` | string |  |
| `statusCode` | number |  |
| `text` | string |  |
| `textAnalysis` | object |  |
| `to` | string |  |
| `unicode` | boolean |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /reports/single/:msgId` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-message.md) for the provider-specific parameters and requirements.

