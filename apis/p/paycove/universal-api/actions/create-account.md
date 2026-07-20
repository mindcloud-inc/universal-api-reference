# Paycove: Create Account

Creates an account in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "countryCode": "string",
  "currency": "string",
  "legalAcceptanceToken": "string",
  "name": "Ava Chen",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "countryCode": "string",
    "currency": "string",
    "legalAcceptanceToken": "string",
    "name": "Ava Chen",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | yes | Two-letter country code for the account. |
| `currency` | string | yes | The account currency. |
| `legalAcceptanceToken` | string | yes | The legal acceptance token returned by the legal-accept flow. |
| `name` | string | yes | The account name. |
| `phone` | string | no | The account phone number. |
| `platformFee` | number | no | Platform fee percentage. |
| `template` | object | no | Template settings for the account. |
| `timezone` | string | yes | The account timezone. |
| `user` | object | no | The initial account user to create. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paycove API returns.

## Native endpoint

Through the native Paycove API, this operation is `POST accounts` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

