# Discourse: List Group Members

Retrieves members of a Discourse group.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-group-members?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-group-members?${params}`, {
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
| `name` | string | yes | Discourse group name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {}
      ],
      "meta": {},
      "owners": [
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
| `members` | array<object> |  |
| `meta` | object |  |
| `owners` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /groups/:name/members.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-members.md) for the provider-specific parameters and requirements.

