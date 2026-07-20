# Certifier: Schedule Credential Issuance

Schedules future credential issuance in Certifier.

```
PUT https://connect.mindcloud.co/v1/universal/certifier/latest/actions/schedule-credential-issuance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/schedule-credential-issuance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "send_at_issuance": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/schedule-credential-issuance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "send_at_issuance": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `issue_at` | date | no | Use an ISO 8601 date-time string. |
| `send_at_issuance` | boolean | yes | Live runtime currently requires this flag when scheduling issuance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customAttributes": {},
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "groupId": "string",
      "id": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "publicId": "string",
      "recipient": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `createdAt` | date |  |
| `customAttributes` | object |  |
| `expiryDate` | date |  |
| `groupId` | string |  |
| `id` | string |  |
| `issueDate` | date |  |
| `publicId` | string |  |
| `recipient` | object |  |
| `recipient.email` | string |  |
| `recipient.id` | string |  |
| `recipient.name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Certifier API, this operation is `POST /credentials/:id/schedule` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-credential-issuance.md) for the provider-specific parameters and requirements.

