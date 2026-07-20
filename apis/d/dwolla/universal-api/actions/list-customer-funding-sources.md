# Dwolla: List Customer Funding Sources

Retrieves funding sources for a Dwolla customer.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-customer-funding-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-customer-funding-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/list-customer-funding-sources?${params}`, {
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
| `id` | string | no | Dwolla customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {},
      "_links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object | Embedded funding source rows returned for the customer. |
| `_links` | object | HAL links for the customer funding-source collection. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /customers/[:id]/funding-sources` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-funding-sources.md) for the provider-specific parameters and requirements.

