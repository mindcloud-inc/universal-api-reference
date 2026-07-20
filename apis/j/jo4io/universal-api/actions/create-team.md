# jo4.io: Create Team



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "teamSlug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "teamSlug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `logoUrl` | string | no |  |
| `name` | string | yes |  |
| `teamSlug` | string | yes |  |

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

Through the native jo4.io API, this operation is `POST /protected/teams` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

