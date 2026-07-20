# Envoice: List Products

Retrieves products from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-products?${params}`, {
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
| `page` | number | no | Result page number. |
| `pageSize` | number | no | Number of results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Count": 1,
      "ErrorMessages": [
        "string"
      ],
      "IsFaulted": true,
      "Result": [
        {}
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Count` | number | Number of products in the current response. |
| `ErrorMessages` | array<string> | Error messages returned by Envoice. |
| `IsFaulted` | boolean | Whether the request failed. |
| `Result` | array<object> | Products returned by Envoice. |
| `TotalCount` | number | Total products matching the query. |

## Native endpoint

Through the native Envoice API, this operation is `GET product/all` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

