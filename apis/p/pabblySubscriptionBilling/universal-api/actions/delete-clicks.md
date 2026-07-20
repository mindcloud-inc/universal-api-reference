# Pabbly Subscription Billing: Delete Clicks



```
DELETE https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-clicks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-clicks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-clicks?${params}`, {
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
      "affiliateEmail": "ava@example.com",
      "affiliateId": "string",
      "commissionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ipAddress": "string",
      "linkId": "https://example.com",
      "linkTitle": "https://example.com",
      "referralUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateEmail` | string |  |
| `affiliateId` | string |  |
| `commissionId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `linkId` | string |  |
| `linkTitle` | string |  |
| `referralUrl` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `DELETE /v1/commissions/clicks/:clickId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-clicks.md) for the provider-specific parameters and requirements.

