# Weberlo: Create Transaction Event

Creates a transaction event in Weberlo.

```
POST https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-transaction-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-transaction-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "time": "1712083200000",
  "transactionId": "order-1001",
  "transactionType": "order-success",
  "transactionAmount": "18000",
  "transactionDescription": "Purchase of wizard stage 3 order"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-transaction-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "time": "1712083200000",
    "transactionId": "order-1001",
    "transactionType": "order-success",
    "transactionAmount": "18000",
    "transactionDescription": "Purchase of wizard stage 3 order"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `time` | number | yes | Transaction timestamp in milliseconds. Example: `1712083200000`. |
| `transactionId` | string | yes | Unique transaction identifier. Example: `order-1001`. |
| `transactionType` | string | yes | Transaction event type. Example: `order-success`. |
| `transactionAmount` | number | yes | Transaction amount. Example: `18000`. |
| `transactionDescription` | string | yes | Transaction description. Example: `Purchase of wizard stage 3 order`. |
| `transactionCurrency` | string | no | Currency code. Example: `USD`. |
| `email` | string | no | Visitor email address. Example: `wizard-stage3+buyer@example.com`. |
| `firstName` | string | no | Visitor first name. Example: `Avery`. |
| `lastName` | string | no | Visitor last name. Example: `Lopez`. |
| `name` | string | no | Visitor full name. Example: `Avery Lopez`. |
| `sessionId` | string | no | Session identifier. Example: `11111111-1111-4111-8111-111111111111`. |
| `platform` | string | no | Commerce or source platform. Example: `stripe`. |
| `platformId` | string | no | Platform-specific identifier. Example: `customer-123`. |
| `country` | string | no | Country code or country value. Example: `US`. |
| `phone` | string | no | Visitor phone number. Example: `928002271555`. |
| `ipAddress` | string | no | Visitor IP address. Example: `1.1.1.1`. |
| `utmSource` | string | no | UTM source. Example: `newsletter`. |
| `utmMedium` | string | no | UTM medium. Example: `email`. |
| `utmCampaign` | string | no | UTM campaign. Example: `spring-launch`. |
| `utmContent` | string | no | UTM content. Example: `hero-cta`. |
| `fbclid` | string | no | Facebook click identifier. Example: `fbclid-value`. |
| `gclid` | string | no | Google click identifier. Example: `gclid-value`. |
| `parentId` | string | no | Parent event or transaction ID. Example: `parent-event-123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weberlo API returns.

## Native endpoint

Through the native Weberlo API, this operation is `POST /event/transaction` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction-event.md) for the provider-specific parameters and requirements.

