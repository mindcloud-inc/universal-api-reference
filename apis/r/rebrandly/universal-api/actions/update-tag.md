# Rebrandly: Update Tag

Updates an existing tag in Rebrandly.

```
PUT https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "cfa87d9986144793b8608026ef7aa50e",
  "name": "mc-tag-0422155742-updated",
  "color": "FF9900"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "cfa87d9986144793b8608026ef7aa50e",
    "name": "mc-tag-0422155742-updated",
    "color": "FF9900"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the tag to update. Example: `cfa87d9986144793b8608026ef7aa50e`. |
| `name` | string | yes | New unique name of the tag. Example: `mc-tag-0422155742-updated`. |
| `color` | string | yes | 6-digit hexadecimal color assigned to the tag. Example: `FF9900`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "clicks": 1,
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "scans": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `clicks` | number |  |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scans` | object |  |

## Native endpoint

Through the native Rebrandly API, this operation is `POST /tags/:id` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

