# Platrum: Save board

Creates or updates a board in Platrum.

```
POST https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/save-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access_blocks[]` | array<object> | no | Block access rules. |
| `access_users[]` | array<object> | no | User access rules. |
| `color_background` | string | no | Board background color. |
| `color_text` | string | no | Board text color. |
| `favourite_states_user_ids[]` | array<string> | no | Users who marked the board favorite. |
| `hidden_panels_are_visible` | boolean | no | Whether hidden panels are visible. |
| `hidden_states_user_ids[]` | array<string> | no | Users who hid the board. |
| `id` | number | no | Board ID for updates. |
| `name` | string | no | Board name. |
| `owner_user_id` | string | no | Board owner user ID. |
| `task_field_keys[]` | array<string> | no | Task field keys shown on the board. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Platrum API, this operation is `POST /tasks/api/board/store` (base URL `https://3e8e7be.platrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-board.md) for the provider-specific parameters and requirements.

