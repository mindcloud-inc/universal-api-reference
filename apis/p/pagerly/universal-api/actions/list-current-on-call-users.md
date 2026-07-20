# Pagerly: List Current On-Call Users

Retrieves current on-call users from Pagerly.

```
GET https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/list-current-on-call-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pagerly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/list-current-on-call-users?connectionId=$CONNECTION_ID&teamName=Select%20a%20Pagerly%20team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamName": "Select a Pagerly team"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerly/latest/actions/list-current-on-call-users?${params}`, {
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
| `teamName` | string | yes | Exact Pagerly team name to query for current on-call users. Example: `Select a Pagerly team`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "imageUrl": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Current on-call user email address. |
| `id` | string | Pagerly user identifier. |
| `imageUrl` | string | Current on-call user avatar image URL when present. |
| `name` | string | Current on-call user name. |

## Native endpoint

Through the native Pagerly API, this operation is `GET /o/currentusers` (base URL `https://api.pagerly.io/pagerly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-on-call-users.md) for the provider-specific parameters and requirements.

