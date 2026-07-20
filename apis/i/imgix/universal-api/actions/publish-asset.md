# imgix: Publish Asset

Publishes an asset in imgix.

```
PUT https://connect.mindcloud.co/v1/universal/imgix/latest/actions/publish-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/publish-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "69de49d580720625c04f9162",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgix/latest/actions/publish-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "69de49d580720625c04f9162",
    "sourceId": "69de49d580720625c04f9162",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |
| `sourceId` | string | yes | The imgix source_id for the asset. Default: `69de49d580720625c04f9162`. |
| `url` | string | yes | The full imgix URL of the asset to publish. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "publishId": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.publishId` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `POST publish` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-asset.md) for the provider-specific parameters and requirements.

