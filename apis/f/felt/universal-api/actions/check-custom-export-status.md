# Felt: Check Custom Export Status

Retrieves custom layer export status from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/check-custom-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/check-custom-export-status?connectionId=$CONNECTION_ID&mapId=string&layerId=string&exportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mapId": "string",
  "layerId": "string",
  "exportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/check-custom-export-status?${params}`, {
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
| `exportId` | string | yes | The ID of the custom export request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "export_id": "string",
      "filters": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string | Download URL for the completed custom export. |
| `export_id` | string | The ID of the custom export request. |
| `filters` | array<object> | Filters used for the export request. |
| `status` | string | Processing status of the export request. |

## Native endpoint

Through the native Felt API, this operation is `GET /maps/:mapId/layers/:layerId/custom_exports/:exportId` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-custom-export-status.md) for the provider-specific parameters and requirements.

