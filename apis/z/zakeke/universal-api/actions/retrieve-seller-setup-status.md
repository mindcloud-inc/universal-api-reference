# Zakeke: Retrieve Seller Setup Status



```
GET https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-seller-setup-status?${params}`, {
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
      "connectedWithEStore": true,
      "firstCustomizableProductCreated": true,
      "freeTrialStarted": true,
      "placeTestOrder": true,
      "requirePaymentInformation": true,
      "signupProcessCompleted": true,
      "trialEnd": "string",
      "trialStart": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectedWithEStore` | boolean |  |
| `firstCustomizableProductCreated` | boolean |  |
| `freeTrialStarted` | boolean |  |
| `placeTestOrder` | boolean |  |
| `requirePaymentInformation` | boolean |  |
| `signupProcessCompleted` | boolean |  |
| `trialEnd` | string |  |
| `trialStart` | string |  |

## Native endpoint

Through the native Zakeke API, this operation is `GET /v2/sellerSetupStatus` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-seller-setup-status.md) for the provider-specific parameters and requirements.

