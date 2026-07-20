# Tarvent: Get Account Invoice

Retrieves an account invoice from Tarvent by ID.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-invoice?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account-invoice?${params}`, {
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
| `variables.id` | string | yes | The Tarvent invoice ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountPaid": 1,
      "billPeriodEndUtc": "2026-05-07T12:00:00.000Z",
      "billPeriodStartUtc": "2026-05-07T12:00:00.000Z",
      "dueUtc": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "pdfDownloadUrl": "https://example.com",
      "status": "string",
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaid` | number |  |
| `billPeriodEndUtc` | date |  |
| `billPeriodStartUtc` | date |  |
| `dueUtc` | date |  |
| `id` | string |  |
| `pdfDownloadUrl` | string |  |
| `status` | string |  |
| `totalAmount` | number |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-invoice.md) for the provider-specific parameters and requirements.

