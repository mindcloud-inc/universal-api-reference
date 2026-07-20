# Certifier: Get Credential

Retrieves detailed credential information from Certifier.

```
GET https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-credential?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Certifier API, this operation is `GET /credentials/:id` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credential.md) for the provider-specific parameters and requirements.

