# Bolna: List SIP Trunks

Retrieves SIP trunks configured in your Bolna account.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-sip-trunks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-sip-trunks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-sip-trunks?${params}`, {
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
| `isActive` | boolean | no | Optional filter for active SIP trunks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow": "string",
      "authType": "string",
      "authUsername": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "directMedia": true,
      "disallow": "string",
      "forceRport": true,
      "gateways": [
        {}
      ],
      "iceSupport": true,
      "id": "string",
      "inboundEnabled": true,
      "ipIdentifiers": [
        {}
      ],
      "isActive": true,
      "name": "Ava Chen",
      "outboundLeadingPlusEnabled": true,
      "phoneNumbers": [
        {}
      ],
      "provider": "string",
      "qualifyFrequency": 1,
      "rtpSymmetric": true,
      "transport": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow` | string |  |
| `authType` | string |  |
| `authUsername` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `directMedia` | boolean |  |
| `disallow` | string |  |
| `forceRport` | boolean |  |
| `gateways` | array<object> |  |
| `iceSupport` | boolean |  |
| `id` | string |  |
| `inboundEnabled` | boolean |  |
| `ipIdentifiers` | array<object> |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `outboundLeadingPlusEnabled` | boolean |  |
| `phoneNumbers` | array<object> |  |
| `provider` | string |  |
| `qualifyFrequency` | number |  |
| `rtpSymmetric` | boolean |  |
| `transport` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /sip-trunks/trunks` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sip-trunks.md) for the provider-specific parameters and requirements.

