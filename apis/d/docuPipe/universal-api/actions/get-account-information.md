# DocuPipe: Get Account Information

Retrieves account information from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "awsContractDetails": {},
      "billingMethod": "string",
      "overageCredits": 1,
      "overageEnabled": true,
      "planCosts": {},
      "planName": "Ava Chen",
      "remainingCredits": 1,
      "renewalDate": "2026-05-07T12:00:00.000Z",
      "retentionDays": 1,
      "upcomingInvoice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awsContractDetails` | object | details about an aws marketplace subscription contract |
| `billingMethod` | string | The billing method for your account: 'free' (no billing), 'direct' (Stripe), or 'aws_marketplace' |
| `overageCredits` | number | The number of overage credits in your account. These credits will be charged on your billing cycle. |
| `overageEnabled` | boolean | Whether or not overage billing is enabled for your account |
| `planCosts` | object | The cost per credit for your account, if applicable |
| `planName` | string | The name of the current plan associated with your account |
| `remainingCredits` | number | The number of remaining credits in your account under your current plan. Consuming these credits will result in no charge |
| `renewalDate` | date | The date on which your current plan will renew |
| `retentionDays` | number | The number of days that your data will be retained. If null, your data has unlimited retention. |
| `upcomingInvoice` | object | Details of the upcoming invoice, including the total amount and the date it will be charged |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /account` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

