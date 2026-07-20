# Hamsa: List User Phone Numbers

Retrieves your phone numbers from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-user-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-user-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/list-user-phone-numbers?${params}`, {
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
| `provider` | string | no |  |
| `skip` | number | no | Default: `1`. |
| `take` | number | no | Default: `10`. |
| `voiceAgentId` | string | no |  |

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
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `type` | string |  |
| `updatedAt` | date |  |
| `voiceAgent.id` | string |  |
| `voiceAgent.name` | string |  |
| `voiceAgentId` | string |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/voice-agents/phone-number/list` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-phone-numbers.md) for the provider-specific parameters and requirements.

