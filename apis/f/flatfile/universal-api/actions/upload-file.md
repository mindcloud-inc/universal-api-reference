# Flatfile: Upload File

Uploads a new file to Flatfile.

```
POST https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environmentId": "us_env_EDBDJn35",
  "file": "example.csv",
  "spaceId": "us_spc_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environmentId": "us_env_EDBDJn35",
    "file": "example.csv",
    "spaceId": "us_spc_mindcloud_flatfile"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentId` | string | yes | Flatfile environment identifier. Default: `us_env_EDBDJn35`. |
| `file` | string | yes | File upload payload. Default: `example.csv`. |
| `spaceId` | string | yes | Flatfile space identifier. Default: `us_spc_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Uploaded file payload. |

## Native endpoint

Through the native Flatfile API, this operation is `POST /files` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

