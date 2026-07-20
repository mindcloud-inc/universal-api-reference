# serviceminder.io: Get Invoice

Retrieves an invoice from ServiceMinder by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-invoice?${params}`, {
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
| `invoiceId` | number | yes | Invoice identifier. |
| `includeContact` | boolean | no | Whether to include contact details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoice": {},
      "message": "string",
      "payments": [
        {}
      ],
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoice` | object |  |
| `message` | string |  |
| `payments` | array<object> |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /invoice/get` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

