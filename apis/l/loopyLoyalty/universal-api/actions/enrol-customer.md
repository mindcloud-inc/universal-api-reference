# Loopy Loyalty: Enrol Customer



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/enrol-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/enrol-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "5fcDywPejwj9QszwngBTKg",
  "firstName": "Taylor",
  "emailAddress": "taylor.stage3@example.com",
  "mobileNumber": "+14155550101"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/enrol-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "5fcDywPejwj9QszwngBTKg",
    "firstName": "Taylor",
    "emailAddress": "taylor.stage3@example.com",
    "mobileNumber": "+14155550101"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Published campaign ID to enrol into. Example: `5fcDywPejwj9QszwngBTKg`. |
| `firstName` | string | yes | Customer first name. Example: `Taylor`. |
| `emailAddress` | string | yes | Customer email address. Example: `taylor.stage3@example.com`. |
| `mobileNumber` | string | yes | Customer mobile number. Example: `+14155550101`. |
| `dataConsentOptIn` | boolean | no | Whether the customer opted into data consent. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeZoneOffset` | string | no | Optional timezone offset in minutes for expiry-aware campaigns. Example: `-300`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pid` | string | Loopy member PID used for downstream card operations. |
| `url` | string | Wallet install URL for the newly enrolled card. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /enrol/:campaignId` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrol-customer.md) for the provider-specific parameters and requirements.

