# Felt: Create Custom Layer Export

Creates a custom layer export in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-custom-layer-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-custom-layer-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "layerId": "string",
  "outputFormat": "CSV"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-custom-layer-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "layerId": "string",
    "outputFormat": "CSV"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map where the layer is located. |
| `layerId` | string | yes | The ID of the layer to export. |
| `outputFormat` | list | yes | The export output format. One of: `CSV`, `GeoJSON`, `GeoPackage`, `GeoTIFF`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailOnCompletion` | boolean | no | Whether Felt should email when the export completes. Default: `false`. |
| `filters[]` | array<object> | no | Optional Felt Style Language filters for the export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "export_request_id": "string",
      "poll_endpoint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `export_request_id` | string | Custom export request identifier. |
| `poll_endpoint` | string | Endpoint to poll for export completion. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/layers/:layerId/custom_export` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-layer-export.md) for the provider-specific parameters and requirements.

