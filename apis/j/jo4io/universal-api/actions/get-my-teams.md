# jo4.io: List My Teams



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-my-teams?${params}`, {
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
| `page` | number | no |  |
| `size` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canCreateUrl": true,
      "createdTime": 1,
      "description": "string",
      "id": 1,
      "logoUrl": "https://example.com",
      "memberCount": 1,
      "modifiedTime": 1,
      "myRole": "string",
      "name": "Ava Chen",
      "ownerEmail": "ava@example.com",
      "ownerId": 1,
      "slug": "string",
      "subscriptionExpiry": 1,
      "subscriptionStatus": "string",
      "subscriptionTier": "string",
      "teamSlug": "string",
      "urlCount": 1,
      "urlLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canCreateUrl` | boolean |  |
| `createdTime` | number |  |
| `description` | string |  |
| `id` | number |  |
| `logoUrl` | string |  |
| `memberCount` | number |  |
| `modifiedTime` | number |  |
| `myRole` | string |  |
| `name` | string |  |
| `ownerEmail` | string |  |
| `ownerId` | number |  |
| `slug` | string |  |
| `subscriptionExpiry` | number |  |
| `subscriptionStatus` | string |  |
| `subscriptionTier` | string |  |
| `teamSlug` | string |  |
| `urlCount` | number |  |
| `urlLimit` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `GET /protected/teams` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-my-teams.md) for the provider-specific parameters and requirements.

