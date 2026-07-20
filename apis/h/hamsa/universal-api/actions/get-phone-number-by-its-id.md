# Hamsa: Get Phone Number by its ID

Retrieves a phone number from Hamsa by ID.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-phone-number-by-its-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-phone-number-by-its-id?connectionId=$CONNECTION_ID&pid=string&pid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pid": "string",
  "pid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-phone-number-by-its-id?${params}`, {
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
| `pid` | string | yes |  |
| `pid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "label": "string",
      "number": "string",
      "sipInboundConfigs": {
        "originationUri": "string"
      },
      "sipOutboundConfigs": {
        "address": "string",
        "transportType": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "voiceAgent": {
        "id": "string",
        "name": "Ava Chen"
      },
      "voiceAgentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `label` | string |  |
| `number` | string |  |
| `sipInboundConfigs.originationUri` | string |  |
| `sipOutboundConfigs.address` | string |  |
| `sipOutboundConfigs.transportType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `voiceAgent.id` | string |  |
| `voiceAgent.name` | string |  |
| `voiceAgentId` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/voice-agents/phone-number` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-phone-number-by-its-id.md) for the provider-specific parameters and requirements.

