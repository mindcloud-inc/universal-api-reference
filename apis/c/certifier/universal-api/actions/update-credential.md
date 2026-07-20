# Certifier: Update Credential

Updates an existing credential in Certifier.

```
PUT https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certifier/latest/actions/update-credential', {
  method: 'PUT',
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
| `id` | string | yes |  |
| `recipient` | object | no |  |
| `recipient.id` | string | no |  |
| `recipient.name` | string | no |  |
| `recipient.email` | string | no |  |
| `issue_date` | date | no | Use YYYY-MM-DD. |
| `expiry_date` | date | no | Use YYYY-MM-DD. |
| `custom_attributes` | object | no | Key-value map of custom attribute tags to values. |

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

Through the native Certifier API, this operation is `PATCH /credentials/:id` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-credential.md) for the provider-specific parameters and requirements.

