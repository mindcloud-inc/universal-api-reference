# Zubie: Apply Tag

Applies a tag in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity_keys[]": [
    "string"
  ],
  "tag_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/apply-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity_keys[]": ["string"],
    "tag_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity_keys[]` | array<string> | yes | Keys of entities to add or remove the tag from. |
| `tag_key` | string | yes | Unique tag key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "entity_keys": [
        "string"
      ],
      "tag_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `entity_keys` | array<string> |  |
| `tag_key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `POST /tag/{tag_key}/apply` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-tag.md) for the provider-specific parameters and requirements.

