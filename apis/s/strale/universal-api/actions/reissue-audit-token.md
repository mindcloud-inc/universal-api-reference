# Strale: Reissue Audit Token

Reissues an audit token for a transaction in Strale.

```
POST https://connect.mindcloud.co/v1/universal/strale/latest/actions/reissue-audit-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strale/latest/actions/reissue-audit-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strale/latest/actions/reissue-audit-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expires_in_days` | number | no | Number of days before the new audit token expires. |
| `id` | string | yes | Transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auditUrl": "https://example.com",
      "expiresAt": 1,
      "expiresAtIso": "2026-05-07T12:00:00.000Z",
      "token": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditUrl` | string | Shareable audit URL. |
| `expiresAt` | number | Audit token expiration as a Unix timestamp. |
| `expiresAtIso` | date | Audit token expiration timestamp in ISO format. |
| `token` | string | Fresh audit token. |
| `transactionId` | string | Transaction identifier. |

## Native endpoint

Through the native Strale API, this operation is `POST /v1/transactions/:id/audit-token` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reissue-audit-token.md) for the provider-specific parameters and requirements.

