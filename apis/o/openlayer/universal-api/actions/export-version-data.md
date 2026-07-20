# Openlayer: Export Version Data

Exports version data from the Openlayer API.

```
POST https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/export-version-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/export-version-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fmt": "json",
  "label": "validation",
  "versionId": "67ef0916-c639-4a06-9309-62e906234bb7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/export-version-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fmt": "json",
    "label": "validation",
    "versionId": "67ef0916-c639-4a06-9309-62e906234bb7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fmt` | string | yes | Export format. Default: `json`. |
| `label` | string | yes | Optional export label. Default: `validation`. |
| `versionId` | string | yes | The project version ID. Default: `67ef0916-c639-4a06-9309-62e906234bb7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskResultId": "string",
      "taskResultUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskResultId` | string |  |
| `taskResultUrl` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `POST /versions/:versionId/export` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-version-data.md) for the provider-specific parameters and requirements.

