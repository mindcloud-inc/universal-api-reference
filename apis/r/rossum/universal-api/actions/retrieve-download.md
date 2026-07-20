# Rossum: Retrieve Download

Retrieves a document download from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-download?connectionId=$CONNECTION_ID&documentsDownloadID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentsDownloadID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-download?${params}`, {
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
| `documentsDownloadID` | number | yes | ID of the Rossum download to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "file_name": "Ava Chen",
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Download content URL. |
| `expires_at` | date | Download expiration timestamp. |
| `file_name` | string | Generated archive filename. |
| `id` | number | Rossum download ID. |
| `url` | string | Download resource URL. |

## Native endpoint

Through the native Rossum API, this operation is `GET /documents/downloads/:documentsDownloadID` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-download.md) for the provider-specific parameters and requirements.

