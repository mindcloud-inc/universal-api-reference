# Teamdeck: List Resources

Retrieves resources from your Teamdeck organization.

```
GET https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-resources?${params}`, {
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

Through the native Teamdeck API, this operation is `GET /resources` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

