# SendMe: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendMe/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | Unique contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthDate": "2026-05-07T12:00:00.000Z",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customValues": [
        {}
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "lastName": "Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "origin": "string",
      "phone": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthDate` | date |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `customValues` | array<object> |  |
| `deletedAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `origin` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native SendMe API, this operation is `GET /api/contacts/:id` (base URL `https://app.sendme123.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

