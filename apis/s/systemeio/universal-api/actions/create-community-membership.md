# Systeme.io: Create Community Membership

Creates a membership in a Systeme.io community.

```
POST https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-community-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-community-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "communityId": "string",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/create-community-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "communityId": "string",
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `communityId` | string | yes | Community identifier. |
| `contactId` | number | yes | Contact ID to grant community access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "communityId": "string",
      "contactId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communityId` | string |  |
| `contactId` | string |  |

## Native endpoint

Through the native Systeme.io API, this operation is `POST /api/community/communities/:communityId/memberships` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-community-membership.md) for the provider-specific parameters and requirements.

