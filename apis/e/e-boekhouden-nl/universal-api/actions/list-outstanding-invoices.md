# e-Boekhouden.nl: List Outstanding Invoices

Retrieves outstanding invoices from e-Boekhouden.nl.

```
GET https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-outstanding-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-outstanding-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&credDeb=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "credDeb": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/list-outstanding-invoices?${params}`, {
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
| `credDeb` | string | yes | Retrieve creditors (`C`) or debtors (`D`). |
| `invoiceNumber` | string | no | Only retrieve invoices with this number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | The number of items to retrieve. |
| `offset` | number | no | The number of items to skip. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `GET /v1/mutation/invoice/outstanding` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-outstanding-invoices.md) for the provider-specific parameters and requirements.

