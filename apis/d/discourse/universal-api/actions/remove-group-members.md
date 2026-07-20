# Discourse: Remove Group Members

Removes members from a Discourse group.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/remove-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/remove-group-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "usernames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/remove-group-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "usernames": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Group id. |
| `usernames` | string | yes | Comma-separated usernames to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "skipped_usernames": [
        "Ava Chen"
      ],
      "success": "string",
      "usernames": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `skipped_usernames` | array<string> |  |
| `success` | string |  |
| `usernames` | array<string> |  |

## Native endpoint

Through the native Discourse API, this operation is `DELETE /groups/:id/members.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-group-members.md) for the provider-specific parameters and requirements.

