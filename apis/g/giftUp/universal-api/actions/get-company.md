# Gift Up: Get Company



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-company?${params}`, {
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
      "canShowCheckout": true,
      "currency": "string",
      "id": "string",
      "isCheckoutLive": true,
      "name": "Ava Chen",
      "onboardingCompleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canShowCheckout` | boolean |  |
| `currency` | string |  |
| `id` | string |  |
| `isCheckoutLive` | boolean |  |
| `name` | string |  |
| `onboardingCompleted` | boolean |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /company` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

