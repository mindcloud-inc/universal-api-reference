# imgix: Unpublish Asset

Unpublishes an asset in imgix.

```
DELETE https://connect.mindcloud.co/v1/universal/imgix/latest/actions/unpublish-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/unpublish-asset?connectionId=$CONNECTION_ID&sourceId=69de49d580720625c04f9162&sourceId=69de49d580720625c04f9162&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "69de49d580720625c04f9162",
  "sourceId": "69de49d580720625c04f9162",
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/unpublish-asset?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |
| `sourceId` | string | yes | The imgix source_id for the asset. Default: `69de49d580720625c04f9162`. |
| `url` | string | yes | The full imgix URL of the asset to unpublish. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "unpublishId": "string"
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
| `data.attributes.unpublishId` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `POST unpublish` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpublish-asset.md) for the provider-specific parameters and requirements.

