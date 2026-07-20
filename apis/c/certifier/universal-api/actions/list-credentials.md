# Certifier: List Credentials

Retrieves all available credentials from Certifier.

```
GET https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credentials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/list-credentials?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customAttributes": {},
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "groupId": "string",
      "id": "string",
      "issueDate": "2026-05-07T12:00:00.000Z",
      "publicId": "string",
      "recipient": {
        "email": "ava@example.com",
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
| `createdAt` | date |  |
| `customAttributes` | object |  |
| `expiryDate` | date |  |
| `groupId` | string |  |
| `id` | string |  |
| `issueDate` | date |  |
| `publicId` | string |  |
| `recipient` | object |  |
| `recipient.email` | string |  |
| `recipient.name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Certifier API, this operation is `GET /credentials` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credentials.md) for the provider-specific parameters and requirements.

