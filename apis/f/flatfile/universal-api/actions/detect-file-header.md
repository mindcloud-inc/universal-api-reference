# Flatfile: Detect File Header

Detects the header row in a Flatfile file.

```
POST https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/detect-file-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/detect-file-header" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "header1,header2\\nvalue1,value2",
  "options": {
    "encoding": "utf-8"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/detect-file-header', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "header1,header2\\nvalue1,value2",
    "options": {"encoding":"utf-8"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes | Sample file data for header detection. Default: `header1,header2\\nvalue1,value2`. |
| `options` | string | yes | Header detection options. Default: `{"encoding":"utf-8"}`. |

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
| `data` | object | Header detection payload. |

## Native endpoint

Through the native Flatfile API, this operation is `POST /files/detect-header` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-file-header.md) for the provider-specific parameters and requirements.

