# Felt: Create Layer Export Link

Retrieves a layer export link from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-layer-export-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-layer-export-link?connectionId=$CONNECTION_ID&mapId=string&layerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string",
  "layerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-layer-export-link?${params}`, {
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
| `mapId` | string | yes | The ID of the map where the layer is located. |
| `layerId` | string | yes | The ID of the layer to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "export_link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `export_link` | string | Direct download link for the exported layer data. |

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/layers/:layerId/get_export_link` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-layer-export-link.md) for the provider-specific parameters and requirements.

