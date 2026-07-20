# TouchBasePro: Validate Email Address

Validates an email address in TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/validate-email-address?${params}`, {
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
      "acceptAll": true,
      "domain": "string",
      "email": "ava@example.com",
      "isDisposable": true,
      "isFree": true,
      "isRole": true,
      "isSuccess": true,
      "qualityScore": 1,
      "reason": "string",
      "result": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | boolean |  |
| `domain` | string |  |
| `email` | string |  |
| `isDisposable` | boolean |  |
| `isFree` | boolean |  |
| `isRole` | boolean |  |
| `isSuccess` | boolean |  |
| `qualityScore` | number |  |
| `reason` | string |  |
| `result` | string |  |
| `user` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /validate/ValidateEmailAddress?email={email}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-address.md) for the provider-specific parameters and requirements.

