# Stormboard: Update Idea

Updates an idea in Stormboard.

```
PUT https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ideaId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/update-idea', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ideaId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | Updated idea color. |
| `data` | string | no | Updated idea content or media data. |
| `ideaId` | number | yes | Idea ID from a Stormboard idea record. |
| `ideaType` | string | no | Updated idea type. |
| `lock` | number | no | Set to 1 to lock the idea, or 0 to leave it unlocked. |
| `shape` | string | no | Updated idea shape. |
| `x` | number | no | Updated X position. |
| `y` | number | no | Updated Y position. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `PUT /ideas/:idea_id` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-idea.md) for the provider-specific parameters and requirements.

