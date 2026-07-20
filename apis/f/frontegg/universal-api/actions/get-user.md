# Frontegg: Get User

Retrieves a user from Frontegg by ID.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The user ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "id": "string",
      "isDisabled": true,
      "isLocked": true,
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "mfaEnrolled": true,
      "name": "Ava Chen",
      "phoneNumber": "string",
      "provider": "string",
      "tenantId": "string",
      "tenantIds": [
        "string"
      ],
      "vendorMetadata": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `isDisabled` | boolean |  |
| `isLocked` | boolean |  |
| `lastLogin` | date |  |
| `metadata` | string |  |
| `mfaEnrolled` | boolean |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `provider` | string |  |
| `tenantId` | string |  |
| `tenantIds` | array<string> |  |
| `vendorMetadata` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/users/v1/:id` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

