# Rebrandly: Create Tag

Creates a new tag in Rebrandly.

```
POST https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "mc-tag-0422155742"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "mc-tag-0422155742"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Unique name of the tag. Example: `mc-tag-0422155742`. |
| `color` | string | no | Hexadecimal color assigned to the tag. Example: `DDEEFF`. |

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

Through the native Rebrandly API, this operation is `POST /tags` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

