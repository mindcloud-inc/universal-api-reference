# imgix: Purge Sub-image

Purges a sub-image from the imgix cache.

```
DELETE https://connect.mindcloud.co/v1/universal/imgix/latest/actions/purge-sub-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/purge-sub-image?connectionId=$CONNECTION_ID&sourceId=69de49d580720625c04f9162&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "69de49d580720625c04f9162",
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/purge-sub-image?${params}`, {
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
| `sourceId` | string | yes | The imgix source_id for the sub-image asset. Default: `69de49d580720625c04f9162`. |
| `url` | string | yes | The fully qualified imgix asset URL to purge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "purgeId": "string"
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
| `data.attributes.purgeId` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `POST purge` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purge-sub-image.md) for the provider-specific parameters and requirements.

