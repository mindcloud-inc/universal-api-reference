# Histre: Retrieve Collection Details

Retrieves collection details from Histre.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-collection-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-collection-details?connectionId=$CONNECTION_ID&bookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-collection-details?${params}`, {
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
| `bookId` | string | yes | Identifier of the Histre collection to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `GET /api/v1/collections/[:book_id]/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-collection-details.md) for the provider-specific parameters and requirements.

