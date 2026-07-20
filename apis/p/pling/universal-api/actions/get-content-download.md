# Pling: Get Content Download

Retrieves a content download URL from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content-download?connectionId=$CONNECTION_ID&contentId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content-download?${params}`, {
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
| `contentId` | string | yes | Pling content identifier to download from. |
| `itemId` | string | yes | Download item number for the content entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_version": "string",
      "downloadlink": "https://example.com",
      "downloadmd5sum": "string",
      "downloadway": "string",
      "mimetype": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_version` | string | File version. |
| `downloadlink` | string | Resolved download URL. |
| `downloadmd5sum` | string | File checksum when provided. |
| `downloadway` | string | OCS download method. |
| `mimetype` | string | Download MIME type. |

## Native endpoint

Through the native Pling API, this operation is `GET /content/download/:contentId/:itemId` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-download.md) for the provider-specific parameters and requirements.

