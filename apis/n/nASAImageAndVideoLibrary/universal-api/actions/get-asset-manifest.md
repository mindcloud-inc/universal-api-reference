# NASA Image and Video Library: Get Asset Manifest

Retrieves an asset manifest from NASA Image and Video Library.

```
GET https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-manifest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NASA Image and Video Library `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-manifest?connectionId=$CONNECTION_ID&nasaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nasaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-manifest?${params}`, {
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
| `nasaId` | string | yes | The NASA media asset ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": {
        "href": "string",
        "items": [
          {
            "href": "string"
          }
        ],
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection.href` | string | Canonical NASA URL for this asset manifest. |
| `collection.items` | array<object> | File and metadata resources available for the asset. |
| `collection.items[].href` | string | One downloadable file or metadata URL from the asset manifest. |
| `collection.version` | string | Collection+JSON version returned by NASA. |

## Native endpoint

Through the native NASA Image and Video Library API, this operation is `GET /asset/:nasa_id` (base URL `https://images-api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-manifest.md) for the provider-specific parameters and requirements.

