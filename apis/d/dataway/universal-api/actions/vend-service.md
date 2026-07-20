# Dataway: Vend Service

Creates a new vend transaction in Dataway.

```
POST https://connect.mindcloud.co/v1/universal/dataway/latest/actions/vend-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/vend-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service_slug": "string",
  "biller_identifier": "string",
  "amount": "string",
  "reference": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataway/latest/actions/vend-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service_slug": "string",
    "biller_identifier": "string",
    "amount": "string",
    "reference": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service_slug` | string | yes | Vendor service slug to vend. |
| `biller_identifier` | string | yes | Customer identifier such as phone number or smartcard number. |
| `variation_slug` | string | no | Optional variation slug when the service requires a variation. |
| `amount` | string | yes | Vend amount in naira when the service accepts arbitrary values. |
| `reference` | string | yes | Unique client reference for the vend request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "commission": 1,
        "date": "2026-05-07T12:00:00.000Z",
        "externalReference": "string",
        "extras": {},
        "reference": "string",
        "status": "string",
        "title": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Vend transaction result. |
| `data.amount` | number | Transaction amount when returned numerically. |
| `data.commission` | number | Provider commission when returned numerically. |
| `data.date` | date | Transaction date. |
| `data.externalReference` | string | Client-supplied reference echoed by the provider. |
| `data.extras` | object | Provider-specific extras object. |
| `data.reference` | string | Provider reference when returned. |
| `data.status` | string | Transaction status. |
| `data.title` | string | Transaction title when returned. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `POST /vend` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vend-service.md) for the provider-specific parameters and requirements.

