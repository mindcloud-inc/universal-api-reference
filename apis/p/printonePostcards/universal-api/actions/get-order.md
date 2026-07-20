# Print.one Postcards: Get Order

Retrieves an order from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | Order ID to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymizedAt": "2026-05-07T12:00:00.000Z",
      "auditLogs": [
        {}
      ],
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "csvOrderId": "string",
      "definitiveCountryId": "string",
      "deliverySpeed": "string",
      "errors": [
        "string"
      ],
      "finish": "string",
      "format": "string",
      "friendlyStatus": "string",
      "id": "string",
      "isBillable": true,
      "mergeVariables": {},
      "metadata": {},
      "recipient": {},
      "region": "string",
      "sendDate": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "status": "string",
      "templateId": "string",
      "templateVersion": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymizedAt` | date |  |
| `auditLogs` | array<object> |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `csvOrderId` | string |  |
| `definitiveCountryId` | string |  |
| `deliverySpeed` | string |  |
| `errors` | array<string> |  |
| `finish` | string |  |
| `format` | string |  |
| `friendlyStatus` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `mergeVariables` | object |  |
| `metadata` | object |  |
| `recipient` | object |  |
| `region` | string |  |
| `sendDate` | date |  |
| `sender` | object |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateVersion` | number |  |
| `updatedAt` | date |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/orders/:id` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

