# Postmaster+: Scan Single Email

Scans a single email in Postmaster+.

```
POST https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/scan-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/scan-single-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/scan-single-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions` | string | no | Comma-separated intelligence actions to run. |
| `email` | string | yes | The email address to scan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "message": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Email address. |
| `id` | number | Single email record ID. |
| `message` | string | Provider message. |
| `status` | string | Deliverability status. |
| `updatedAt` | string | Update timestamp. |

## Native endpoint

Through the native Postmaster+ API, this operation is `POST /api/v1/intelligence/single-emails/scan` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-single-email.md) for the provider-specific parameters and requirements.

