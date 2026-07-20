# Sarbacane: Get Credits

Retrieves account credit details from Sarbacane.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits?${params}`, {
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
      "count": 1,
      "creditType": "string",
      "expirationDate": "string",
      "subscriptionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Remaining credits available for the subscription type and credit type. |
| `creditType` | string | Sarbacane credit type, such as EMAIL_CAMPAIGNS, SMS, or EMAIL_SENDKIT. |
| `expirationDate` | string | Expiration date for this credit allocation, if any. |
| `subscriptionType` | string | Subscription cadence associated with the credit allocation. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /credits` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credits.md) for the provider-specific parameters and requirements.

