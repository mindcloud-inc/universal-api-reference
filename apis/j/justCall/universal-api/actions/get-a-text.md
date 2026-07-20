# JustCall: Get a Text

Retrieves a text from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-text?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-text?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentEmail": "ava@example.com",
      "agentId": 1,
      "agentName": "Ava Chen",
      "contactEmail": "ava@example.com",
      "contactName": "Ava Chen",
      "contactNumber": "string",
      "costIncurred": 1,
      "deliveryStatus": "string",
      "direction": "string",
      "id": 1,
      "isDeleted": true,
      "justcallLineName": "Ava Chen",
      "justcallNumber": "string",
      "medium": "string",
      "smsDate": "string",
      "smsInfo": {},
      "smsTime": "string",
      "smsUserDate": "string",
      "smsUserTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentEmail` | string |  |
| `agentId` | number |  |
| `agentName` | string |  |
| `contactEmail` | string |  |
| `contactName` | string |  |
| `contactNumber` | string |  |
| `costIncurred` | number |  |
| `deliveryStatus` | string |  |
| `direction` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `justcallLineName` | string |  |
| `justcallNumber` | string |  |
| `medium` | string |  |
| `smsDate` | string |  |
| `smsInfo` | object |  |
| `smsTime` | string |  |
| `smsUserDate` | string |  |
| `smsUserTime` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/texts/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-text.md) for the provider-specific parameters and requirements.

