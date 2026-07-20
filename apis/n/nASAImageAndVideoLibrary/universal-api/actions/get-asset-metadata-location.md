# NASA Image and Video Library: Get Asset Metadata Location

Retrieves an asset metadata URL from NASA Image and Video Library.

```
GET https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-metadata-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NASA Image and Video Library `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-metadata-location?connectionId=$CONNECTION_ID&nasaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nasaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-asset-metadata-location?${params}`, {
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
| `nasaId` | string | yes | The NASA media asset ID whose metadata location to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | string | Direct URL to the asset metadata JSON document. |

## Native endpoint

Through the native NASA Image and Video Library API, this operation is `GET /metadata/:nasa_id` (base URL `https://images-api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-metadata-location.md) for the provider-specific parameters and requirements.

