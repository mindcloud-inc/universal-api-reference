# Zubie: Update Tag

Updates an existing tag in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag_key` | string | yes | Unique tag key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "key": "string",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `key` | string |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /tag/{tag_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

