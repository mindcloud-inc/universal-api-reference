# Harvestr.io: List Users



```
GET https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvestr.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvestr/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBefore` | date | no | Filter items created before this date (ISO 8601 format) |
| `createdAfter` | date | no | Filter items created after this date (ISO 8601 format) |
| `updatedBefore` | date | no | Filter items updated before this date (ISO 8601 format) |
| `updatedAfter` | date | no | Filter items updated after this date (ISO 8601 format) |
| `email` | string | no | Filter users by email address |
| `companyId` | string | no | Filter users by company ID |
| `externalUid` | string | no | Filter users by external unique identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalUid": "string",
      "id": "string",
      "importId": "string",
      "name": "Ava Chen",
      "phone": "string",
      "segments": {
        "clientId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | Client identifier |
| `companyId` | string | Identifier of the company the user belongs to |
| `createdAt` | date | Creation date of the user |
| `email` | string | Email address of the user (can be empty) |
| `externalUid` | string | Only defined when external uid has been setup in Harvestr and when the entity has an external uid in source |
| `id` | string | Unique identifier of the user |
| `importId` | string | Only defined when the user was created from XLSX import, equal to its defined ID |
| `name` | string | Name of the user |
| `phone` | string | Phone number of the user |
| `segments` | array<object> | Segments associated with this user |
| `segments.clientId` | string | Client identifier |
| `segments.createdAt` | date | Creation date of the segment |
| `segments.id` | string | Unique identifier of the segment |
| `segments.name` | string | Name of the segment |
| `segments.updatedAt` | date | Last update date of the segment |
| `type` | string | Type of the user |
| `updatedAt` | date | Last update date of the user |

## Native endpoint

Through the native Harvestr.io API, this operation is `GET /user` (base URL `https://rest.harvestr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

