# Teamdeck: Get Resource

Retrieves a resource from your Teamdeck organization.

```
GET https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-resource?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/get-resource?${params}`, {
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
| `id` | number | yes | The Teamdeck resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "canSeeCalendar": true,
      "contractEndDate": "string",
      "contractStartDate": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "isPartTime": true,
      "isVisible": true,
      "name": "Ava Chen",
      "organizationUnitId": 1,
      "role": "string",
      "scimId": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `canSeeCalendar` | boolean |  |
| `contractEndDate` | string |  |
| `contractStartDate` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `isPartTime` | boolean |  |
| `isVisible` | boolean |  |
| `name` | string |  |
| `organizationUnitId` | number |  |
| `role` | string |  |
| `scimId` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Teamdeck API, this operation is `GET /resources/:id` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

