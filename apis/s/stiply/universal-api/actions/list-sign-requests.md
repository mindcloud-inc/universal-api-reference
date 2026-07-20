# Stiply: List Sign Requests

Retrieves sign requests available in Stiply.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-sign-requests?${params}`, {
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
| `status` | string | no | When provided, only sign requests with the provided status are fetched. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allSignedAt": "string",
      "callBackUrl": "https://example.com",
      "canceledAt": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "string",
      "externalKey": "string",
      "id": 1,
      "key": "string",
      "rejectedAt": "string",
      "sentAt": "string",
      "signingSequenceType": "string",
      "signingType": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allSignedAt` | string |  |
| `callBackUrl` | string |  |
| `canceledAt` | string |  |
| `createdAt` | date |  |
| `expiresAt` | string |  |
| `externalKey` | string |  |
| `id` | number |  |
| `key` | string |  |
| `rejectedAt` | string |  |
| `sentAt` | string |  |
| `signingSequenceType` | string |  |
| `signingType` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sign-requests.md) for the provider-specific parameters and requirements.

