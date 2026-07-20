# EmailListVerify: Get Credits

Retrieves your available credits from EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits?${params}`, {
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
      "onDemand": {
        "available": 1
      },
      "subscription": {
        "available": 1,
        "expiresAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `onDemand` | object | On-demand credit balance block. |
| `onDemand.available` | number | Remaining on-demand credits. |
| `subscription` | object | Subscription credit balance block, or null. |
| `subscription.available` | number | Remaining subscription credits. |
| `subscription.expiresAt` | date | Subscription expiration timestamp. |

## Native endpoint

Through the native EmailListVerify API, this operation is `GET /api/credits` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

