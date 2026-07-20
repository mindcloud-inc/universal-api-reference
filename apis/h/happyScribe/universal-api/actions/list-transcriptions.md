# HappyScribe: List Transcriptions

Retrieves transcriptions from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-transcriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-transcriptions?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/list-transcriptions?${params}`, {
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
| `folderId` | string | no | Optional folder ID to scope the list to a folder and its subfolders. |
| `organizationId` | string | yes | Workspace organization ID required by HappyScribe for listing transcriptions. |
| `page` | number | no | Optional page number. |
| `tags` | string | no | Optional list of tags to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Pagination links, including next page when available. |
| `results` | array<object> | Transcription metadata results. |

## Native endpoint

Through the native HappyScribe API, this operation is `GET /transcriptions` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transcriptions.md) for the provider-specific parameters and requirements.

