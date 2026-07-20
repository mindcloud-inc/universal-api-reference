# Certs 365: Issue Certificate

Creates a certificate in Certs 365.

```
POST https://connect.mindcloud.co/v1/universal/certs365/latest/actions/issue-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/issue-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "certificateNumber": "string",
  "name": "Ava Chen",
  "course": "string",
  "grantDate": "2026-05-07T12:00:00.000Z",
  "expirationDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certs365/latest/actions/issue-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "certificateNumber": "string",
    "name": "Ava Chen",
    "course": "string",
    "grantDate": "2026-05-07T12:00:00.000Z",
    "expirationDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Issuer email. |
| `certificateNumber` | string | yes | Certificate number. |
| `name` | string | yes | Name associated with the certificate. |
| `course` | string | yes | Course name associated with the certificate. |
| `grantDate` | date | yes | Certificate grant date. |
| `expirationDate` | date | yes | Certificate expiration date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "polygonLink": "https://example.com",
      "qrCodeImage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object |  |
| `message` | string |  |
| `polygonLink` | string |  |
| `qrCodeImage` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/issue` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-certificate.md) for the provider-specific parameters and requirements.

