# Postpone: List Social Accounts

Retrieves social accounts from Postpone.

```
GET https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-social-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-social-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-social-accounts?${params}`, {
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
| `variables.platform` | string | no | Optional platform filter such as reddit, twitter, instagram, facebook, threads, bluesky, linkedin, or pinterest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "followers": 1,
      "formattedUsername": "Ava Chen",
      "id": "string",
      "isConnected": true,
      "isEnabled": true,
      "name": "Ava Chen",
      "platform": "string",
      "profileUrl": "https://example.com",
      "username": "Ava Chen",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `followers` | number |  |
| `formattedUsername` | string |  |
| `id` | string |  |
| `isConnected` | boolean |  |
| `isEnabled` | boolean |  |
| `name` | string |  |
| `platform` | string |  |
| `profileUrl` | string |  |
| `username` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-social-accounts.md) for the provider-specific parameters and requirements.

