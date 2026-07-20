# SeaTable: Get Custom Folder Download Link

Retrieves a download link for a SeaTable custom folder.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-custom-folder-download-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-custom-folder-download-link?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-custom-folder-download-link?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadLink` | string |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api/v2.1/dtable/custom/app-download-link/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-folder-download-link.md) for the provider-specific parameters and requirements.

