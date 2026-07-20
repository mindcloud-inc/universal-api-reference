# Airparser: Get Extended Document Details

Retrieves extended document details from Airparser.

```
GET https://connect.mindcloud.co/v1/universal/airparser/latest/actions/get-extended-document-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/get-extended-document-details?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airparser/latest/actions/get-extended-document-details?${params}`, {
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
| `documentId` | string | yes | The Airparser document ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airparser API returns.

## Native endpoint

Through the native Airparser API, this operation is `GET /docs/:document_id/extended` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extended-document-details.md) for the provider-specific parameters and requirements.

