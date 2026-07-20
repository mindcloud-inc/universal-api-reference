# Felt: Add Layer From Data Source

Creates a map layer from a data source in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/add-layer-from-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/add-layer-from-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "from": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/add-layer-from-data-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "from": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | Map ID that will receive the new layer. |
| `from` | string | yes | Source-layer creation mode: dataset, sql, or stac. |
| `datasetId` | string | no | Dataset ID when from=dataset. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | no | Source ID when from=sql or from=stac. |
| `query` | string | no | SQL query when from=sql. |
| `stacAssetUrl` | string | no | STAC asset URL when from=stac. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object | Links to the map and queued layer group. |
| `status` | string | Layer creation queue status. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/add_source_layer` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-layer-from-data-source.md) for the provider-specific parameters and requirements.

