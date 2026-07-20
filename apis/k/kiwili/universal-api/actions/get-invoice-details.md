# Kiwili: Get Invoice Details

Retrieves details for an invoice in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-details?connectionId=$CONNECTION_ID&invoice_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoice_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-invoice-details?${params}`, {
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
| `invoice_id` | number | yes | The Kiwili invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "EnterpriseId": 1,
      "Id": 1,
      "Number": "string",
      "Status": "string",
      "TotalNoTax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `EnterpriseId` | number |  |
| `Id` | number |  |
| `Number` | string |  |
| `Status` | string |  |
| `TotalNoTax` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /invoice/:invoice_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-details.md) for the provider-specific parameters and requirements.

