# imgix: Get Asset

Retrieves an asset from an imgix source.

```
GET https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-asset?connectionId=$CONNECTION_ID&originPath=string&sourceId=69de49d580720625c04f9162" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "originPath": "string",
  "sourceId": "69de49d580720625c04f9162"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/get-asset?${params}`, {
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
| `originPath` | string | yes | The origin path for the asset in the source. |
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
          "fileSize": 1,
          "mediaHeight": 1,
          "mediaKind": "string",
          "mediaWidth": 1,
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
| `data.attributes.fileSize` | number |  |
| `data.attributes.mediaHeight` | number |  |
| `data.attributes.mediaKind` | string |  |
| `data.attributes.mediaWidth` | number |  |
| `data.attributes.originPath` | string |  |
| `data.attributes.sourceId` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native imgix API, this operation is `GET sources/:sourceId/assets/:originPath` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

