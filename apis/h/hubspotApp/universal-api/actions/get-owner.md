# HubSpot: Get Owner

Retrieves an owner from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-owner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-owner?connectionId=$CONNECTION_ID&ownerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ownerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-owner?${params}`, {
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
| `ownerId` | string | yes | The identifier of the owner to retrieve. |
| `archived` | boolean | no | Whether to return archived owners. |
| `idProperty` | string | no | The identifier type for ownerId, such as the HubSpot owner id or the owner userId. |

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
      "teams": [
        {}
      ],
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
| `archived` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `teams` | array<object> |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `userIdIncludingInactive` | number |  |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/owners/:ownerId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-owner.md) for the provider-specific parameters and requirements.

