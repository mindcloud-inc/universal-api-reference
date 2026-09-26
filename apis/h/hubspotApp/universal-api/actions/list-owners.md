# HubSpot: List Owners

Retrieves owners from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-owners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-owners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-owners?${params}`, {
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
| `email` | string | no | The email address of the owner to return. |
| `archived` | boolean | no | Whether to return archived owners. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "userIdIncludingInactive": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the owner is archived. |
| `createdAt` | date | When the owner was created. |
| `email` | string | The owner's email address. |
| `firstName` | string | The owner's first name. |
| `id` | string | The owner record ID. |
| `lastName` | string | The owner's last name. |
| `type` | string | The owner type. |
| `updatedAt` | date | When the owner was last updated. |
| `userId` | number | The owner's user ID. |
| `userIdIncludingInactive` | number | The owner's user ID including inactive users. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/owners/` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-owners.md) for the provider-specific parameters and requirements.

