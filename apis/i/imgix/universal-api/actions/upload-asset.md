# imgix: Upload Asset

Uploads an asset to an imgix source.

```
POST https://connect.mindcloud.co/v1/universal/imgix/latest/actions/upload-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/upload-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "originPath": "string",
  "sourceId": "69de49d580720625c04f9162"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgix/latest/actions/upload-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "originPath": "string",
    "sourceId": "69de49d580720625c04f9162"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `originPath` | string | yes | The destination origin path for the uploaded asset. |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "contentType": "string",
          "mediaKind": "string",
          "originPath": "string",
          "sourceId": "string"
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
| `data.attributes.contentType` | string |  |
| `data.attributes.mediaKind` | string |  |
| `data.attributes.originPath` | string |  |
| `data.attributes.sourceId` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `POST sources/:sourceId/upload/:originPath` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-asset.md) for the provider-specific parameters and requirements.

