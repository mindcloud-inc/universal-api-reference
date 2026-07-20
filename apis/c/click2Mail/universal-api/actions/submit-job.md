# Click2Mail: Submit Job

Submits an existing job in Click2Mail.

```
PUT https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/submit-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/submit-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "billingType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/submit-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "billingType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | job id |
| `billingType` | string | yes | Payment Method |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingName` | string | no | Name as on the card, Required (Credit Card only) |
| `billingCompany` | string | no | Company |
| `billingAddress1` | string | no | Street address line 1, Required (Credit Card only) |
| `billingAddress2` | string | no | Street address line 2 |
| `billingAddress3` | string | no | Street address line 3 |
| `billingCity` | string | no | City, Required (Credit Card only) |
| `billingState` | string | no | State, Required (Credit Card only) |
| `billingCountry` | string | no | Requires for non USA addresses |
| `billingZip` | string | no | Zip code, Required (Credit Card only) |
| `billingNumber` | string | no | Credit card number, Required (Credit Card only) |
| `billingMonth` | string | no | Expiration month, 2 digits, Required (Credit Card only) |
| `billingYear` | string | no | Expiration year, 2 digits, Required (Credit Card only) |
| `billingCvv` | string | no | Credit card verification code, 3 digits, Required (Credit Card only) |
| `billingCcType` | string | no | Credit card type, Required (Credit Card only) |
| `shipName` | string | no | Shipping address Name |
| `shipOrganization` | string | no | Shipping address Organization |
| `shipAddress1` | string | no | Shipping address line 1 |
| `shipaddress2` | string | no | Shipping address line 2 |
| `shipCity` | string | no | Ship address City |
| `shipState` | string | no | Ship address State |
| `shipZip` | string | no | Ship address Zip code |
| `shipCountry` | string | no | Leave blank for USA |
| `shipperName` | string | no | Shipper |
| `shipMethod` | string | no | Shipping Method |
| `couponCode` | string | no | Coupon Code for order |
| `opaqueDataValue` | string | no | Apple Pay/Google Pay opaque Data Value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `POST /molpro/jobs/{id}/submit` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-job.md) for the provider-specific parameters and requirements.

