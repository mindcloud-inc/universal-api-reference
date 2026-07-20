# Ugosign: Create Envelope

Creates a new envelope in Ugosign.

```
POST https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-envelope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-envelope" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string",
  "deliveryMode": "string",
  "initiatorId": "string",
  "level": "string",
  "recipients": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/create-envelope', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string",
    "deliveryMode": "string",
    "initiatorId": "string",
    "level": "string",
    "recipients": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowRefusal` | string | no |  |
| `contractId` | string | yes |  |
| `deliveryMode` | string | yes |  |
| `expiresAt` | string | no |  |
| `initials` | string | no |  |
| `initiatorId` | string | yes |  |
| `level` | string | yes |  |
| `message` | string | no |  |
| `recipients` | list<string> | yes |  |
| `reminder` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowRefusal": true,
      "contractId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "initials": true,
      "initiatorId": "string",
      "keepOrder": true,
      "level": "string",
      "message": "string",
      "reminder": 1,
      "sealedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowRefusal` | boolean |  |
| `contractId` | string |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `initials` | boolean |  |
| `initiatorId` | string |  |
| `keepOrder` | boolean |  |
| `level` | string |  |
| `message` | string |  |
| `reminder` | number |  |
| `sealedAt` | date |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ugosign API, this operation is `POST /v1/envelopes` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-envelope.md) for the provider-specific parameters and requirements.

