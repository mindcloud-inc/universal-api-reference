# BASIC: Create a new team

Creates a new team in BASIC.

```
POST https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-new-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-new-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/create-a-new-team', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "owner": "string",
        "slug": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.created_at` | date |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.owner` | string |  |
| `data.slug` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `POST /team/` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-team.md) for the provider-specific parameters and requirements.

