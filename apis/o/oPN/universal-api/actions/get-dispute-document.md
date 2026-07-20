# OPN: Get Dispute Document

Retrieves details for a dispute document from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-dispute-document?${params}`, {
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
      "created_at": "string",
      "deleted": true,
      "download_uri": "string",
      "filename": "Ava Chen",
      "id": "string",
      "kind": "string",
      "livemode": true,
      "location": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `download_uri` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /disputes/:id/documents/:documentId` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dispute-document.md) for the provider-specific parameters and requirements.

