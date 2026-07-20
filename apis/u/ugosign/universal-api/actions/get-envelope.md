# Ugosign: Get Envelope

Retrieves an envelope from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-envelope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-envelope?connectionId=$CONNECTION_ID&envelope=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelope": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-envelope?${params}`, {
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
| `envelope` | string | yes |  |

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

Through the native Ugosign API, this operation is `GET /v1/envelopes/:envelope` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-envelope.md) for the provider-specific parameters and requirements.

