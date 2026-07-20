# Honeybadger: Upload Source Map

Uploads a source map to Honeybadger.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/upload-source-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/upload-source-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "minified_url": "https://example.com",
  "minified_file": "string",
  "source_map": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/upload-source-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "minified_url": "https://example.com",
    "minified_file": "string",
    "source_map": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minified_url` | string | yes | Absolute production URL for the minified JavaScript file. |
| `minified_file` | file | yes | The compiled minified JavaScript file. |
| `source_map` | file | yes | The source map file to upload. |
| `revision` | string | no | Deploy revision or code version for the uploaded source map. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Honeybadger source map upload status value returned after a successful upload. |

## Native endpoint

Through the native Honeybadger API, this operation is `POST /source_maps` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-source-map.md) for the provider-specific parameters and requirements.

