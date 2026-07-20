# Discourse: List User Actions

Retrieves recent user actions from Discourse.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-actions?connectionId=$CONNECTION_ID&filter=string&offset=string&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "string",
  "offset": "string",
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-user-actions?${params}`, {
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
| `filter` | string | yes | User action filter value documented by Discourse. |
| `offset` | string | yes | Zero-based offset into the user actions feed. |
| `username` | string | yes | Discourse username whose actions should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user_actions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user_actions` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /user_actions.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-actions.md) for the provider-specific parameters and requirements.

