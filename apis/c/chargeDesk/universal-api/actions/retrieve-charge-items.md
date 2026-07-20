# ChargeDesk: Retrieve Charge Items

Retrieves charge items from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge-items?connectionId=$CONNECTION_ID&chargeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/retrieve-charge-items?${params}`, {
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
| `chargeId` | string | yes | Charge ID whose line items should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "items": [
          {}
        ],
        "taxes": [
          {}
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.items` | array<object> |  |
| `data.taxes` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /charges/:CHARGE_ID/items` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-charge-items.md) for the provider-specific parameters and requirements.

