# Blue: List Company Invoices

Retrieves invoices for a Blue company.

```
GET https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-company-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-company-invoices?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-company-invoices?${params}`, {
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
| `companyId` | string | yes | Blue company node ID. |
| `limit` | number | no | Maximum number of invoices to return. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "hostedUrl": "https://example.com",
      "id": "string",
      "pdfUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `date` | date |  |
| `hostedUrl` | string |  |
| `id` | string |  |
| `pdfUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Blue API, this operation is `POST /graphql` (base URL `https://api.blue.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-invoices.md) for the provider-specific parameters and requirements.

