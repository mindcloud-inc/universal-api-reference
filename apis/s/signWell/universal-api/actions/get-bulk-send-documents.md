# SignWell: Get Bulk Send Documents

Retrieves documents for a bulk send in SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-documents?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-bulk-send-documents?${params}`, {
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
| `id` | string | yes | Unique identifier for a bulk send. |
| `limit` | number | no | Number of documents to fetch. Defaults to 10, max is 50. |
| `page` | number | no | Page number for pagination. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SignWell API returns.

## Native endpoint

Through the native SignWell API, this operation is `GET /bulk_sends/:id/documents` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-send-documents.md) for the provider-specific parameters and requirements.

