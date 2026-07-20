# Zubie: Apply Group Memberships

Applies group memberships in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-group-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-group-memberships" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "group_keys[]": [
    "string"
  ],
  "member_keys[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-group-memberships', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "group_keys[]": ["string"],
    "member_keys[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | The action to apply. One of add, remove, or replace. |
| `group_keys[]` | array<string> | yes | List of group keys to apply. |
| `member_keys[]` | array<string> | yes | List of member entity keys to act on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "group_keys": [
        "string"
      ],
      "member_keys": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `group_keys` | array<string> |  |
| `member_keys` | array<string> |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /groups/apply` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-group-memberships.md) for the provider-specific parameters and requirements.

