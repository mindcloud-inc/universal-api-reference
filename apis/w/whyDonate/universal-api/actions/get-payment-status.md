# WhyDonate: Get Payment Status



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-payment-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-payment-status?connectionId=$CONNECTION_ID&slug=save-the-children" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "save-the-children"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-payment-status?${params}`, {
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
| `slug` | string | yes | Fundraiser slug used when checking payment status. Example: `save-the-children`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargesEnabled": true,
      "detailsSubmitted": true,
      "onboardingApproval": "string",
      "payoutEnabled": true,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargesEnabled` | boolean |  |
| `detailsSubmitted` | boolean |  |
| `onboardingApproval` | string |  |
| `payoutEnabled` | boolean |  |
| `status` | boolean |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/payment/status/` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-status.md) for the provider-specific parameters and requirements.

