# Pabbly Subscription Billing: Get Hosted Page Data



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-hosted-page-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-hosted-page-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-hosted-page-data?${params}`, {
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
      "user": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currency": "string",
        "dateFormat": "string",
        "email": "ava@example.com",
        "facebookUrl": "https://example.com",
        "firstName": "Ava",
        "ipAddress": "string",
        "lastName": "Chen",
        "mobile": "string",
        "phone": "string",
        "state": "string",
        "timeZone": "string",
        "twitterUrl": "https://example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "verified": "string",
        "zipCode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user.addressLine1` | string |  |
| `user.addressLine2` | string |  |
| `user.city` | string |  |
| `user.country` | string |  |
| `user.createdAt` | date |  |
| `user.currency` | string |  |
| `user.dateFormat` | string |  |
| `user.email` | string |  |
| `user.facebookUrl` | string |  |
| `user.firstName` | string |  |
| `user.ipAddress` | string |  |
| `user.lastName` | string |  |
| `user.mobile` | string |  |
| `user.phone` | string |  |
| `user.state` | string |  |
| `user.timeZone` | string |  |
| `user.twitterUrl` | string |  |
| `user.updatedAt` | date |  |
| `user.verified` | string |  |
| `user.zipCode` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/hostedpage` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hosted-page-data.md) for the provider-specific parameters and requirements.

