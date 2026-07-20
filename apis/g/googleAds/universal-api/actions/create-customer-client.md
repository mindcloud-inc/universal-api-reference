# Google Ads: Create Customer Client

Creates a customer client in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-customer-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-customer-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "4556174691",
  "customerClient": {},
  "customerClient.descriptiveName": "MindCloud Test Child Account",
  "customerClient.currencyCode": "USD",
  "customerClient.timeZone": "America/New_York"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-customer-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "4556174691",
    "customerClient": {},
    "customerClient.descriptiveName": "MindCloud Test Child Account",
    "customerClient.currencyCode": "USD",
    "customerClient.timeZone": "America/New_York"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | Manager customer ID under which the child account will be created (without dashes). Default: `4556174691`. Example: `4556174691`. |
| `customerClient` | object | yes | Customer client settings for the new child account. |
| `customerClient.descriptiveName` | string | yes | Display name for the new child customer account. Example: `MindCloud Test Child Account`. |
| `customerClient.currencyCode` | string | yes | ISO 4217 currency code for the new account, for example USD. Default: `USD`. Example: `USD`. |
| `customerClient.timeZone` | string | yes | IANA time zone for the new account, for example America/New_York. Default: `America/New_York`. Example: `America/New_York`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validateOnly` | boolean | no | When true, validates request without creating the account. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string | Resource name of the newly created customer client account. |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:createCustomerClient` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-client.md) for the provider-specific parameters and requirements.

