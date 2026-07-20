# OPN: Delete Dispute Document

Deletes an existing dispute document from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-dispute-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-dispute-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-dispute-document?${params}`, {
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

Through the native OPN API, this operation is `DELETE /disputes/:id/documents/:documentId` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dispute-document.md) for the provider-specific parameters and requirements.

