# Merit: Get Sales Invoice Details



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-details?connectionId=$CONNECTION_ID&Id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-sales-invoice-details?${params}`, {
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
| `Id` | string | yes | Sales invoice ID from Merit docs. |
| `AddAttachment` | boolean | no | Include attachment file content when true. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Attachment": {},
      "Header": {},
      "Lines": [
        {}
      ],
      "Payments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Attachment` | object |  |
| `Header` | object |  |
| `Lines` | array<object> |  |
| `Payments` | array<object> |  |

## Native endpoint

Through the native Merit API, this operation is `POST v2/getinvoice` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-invoice-details.md) for the provider-specific parameters and requirements.

