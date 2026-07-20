# Scanova: Update Tag



```
PUT https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | number | yes | Tag ID |
| `name` | string | no | Tag name |
| `color` | string | no | Tag color (hex code) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created` | date |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Scanova API, this operation is `PUT /tags/{tag_id}/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

