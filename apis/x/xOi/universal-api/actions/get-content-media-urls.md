# XOi: Get Content Media URLs



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content-media-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content-media-urls?connectionId=$CONNECTION_ID&contentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content-media-urls?${params}`, {
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
| `contentIds[]` | array<string> | yes | XOi content IDs to retrieve, up to 50. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jobIds": [
        "string"
      ],
      "lengthBytes": 1,
      "mediaType": "string",
      "orgID": "string",
      "sha256hex": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadedAt": "2026-05-07T12:00:00.000Z",
      "uploader": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Content creation timestamp. |
| `id` | string | The XOi content ID. |
| `jobIds` | array<string> | Associated XOi job IDs. |
| `lengthBytes` | number | Content size in bytes. |
| `mediaType` | string | The content media type. |
| `orgID` | string | The owning XOi organization ID. |
| `sha256hex` | string | SHA-256 content hash. |
| `updatedAt` | date | Content update timestamp when present. |
| `uploadedAt` | date | Content upload timestamp. |
| `uploader` | string | Content uploader. |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-content-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-media-urls.md) for the provider-specific parameters and requirements.

