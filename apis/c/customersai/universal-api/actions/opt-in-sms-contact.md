# Customers.ai: Opt-In SMS Contact

Opts a new SMS contact into a promoter in Customers.ai.

```
POST https://connect.mindcloud.co/v1/universal/customersai/latest/actions/opt-in-sms-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customers.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/opt-in-sms-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "promoterId": 1,
  "smsNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customersai/latest/actions/opt-in-sms-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "promoterId": 1,
    "smsNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `promoterId` | number | yes | Promoter ID to use for the SMS opt-in flow. |
| `smsNumber` | string | yes | Phone number to opt in. |
| `firstName` | string | no | First name of the SMS contact. |
| `lastName` | string | no | Last name of the SMS contact. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Customers.ai API returns.

## Native endpoint

Through the native Customers.ai API, this operation is `PUT /promoters/:id/optin_sms_contact` (base URL `https://api.mobilemonkey.com/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/opt-in-sms-contact.md) for the provider-specific parameters and requirements.

