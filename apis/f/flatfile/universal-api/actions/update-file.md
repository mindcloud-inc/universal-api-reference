# Flatfile: Update File

Updates an existing file in Flatfile.

```
PUT https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "us_fil_mindcloud_flatfile"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "us_fil_mindcloud_flatfile"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | Flatfile file identifier. Default: `us_fil_mindcloud_flatfile`. |

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
| `data` | object | Updated file payload. |

## Native endpoint

Through the native Flatfile API, this operation is `PATCH /files/:fileId` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

