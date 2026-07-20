# OneDeck: Invite Share Studio User

Invites a user to OneDeck Share Studio.

```
POST https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/invite-share-studio-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/invite-share-studio-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shareId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
  "email": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDeck/latest/actions/invite-share-studio-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shareId": "1ff5d564-2ea6-4053-8c20-fac2ef32f029",
    "email": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shareId` | string | yes | Share Studio identifier. Example: `1ff5d564-2ea6-4053-8c20-fac2ef32f029`. |
| `email` | string | yes | Email address to invite. Example: `apps@mindcloud.co`. |
| `firstName` | string | no | Invitee first name. Example: `MindCloud`. |
| `lastName` | string | no | Invitee last name. Example: `Automation`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | no | Record identifier to scope the invitation. Example: `1f242e49-767e-42e0-b16f-3c0a117b4c8e`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDeck API returns.

## Native endpoint

Through the native OneDeck API, this operation is `POST /share-studio/:shareId/invite` (base URL `https://{{credentials.accountName}}.onedeck.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-share-studio-user.md) for the provider-specific parameters and requirements.

