# Trolley: Search Invoices

Finds invoices in Trolley using search filters.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/search-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/search-invoices?${params}`, {
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
| `page` | number | no | Page number |
| `pageSize` | number | no | Page size |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": [
        {}
      ],
      "meta": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoices` | array<object> |  |
| `meta` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `POST /v1/invoices/search` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

