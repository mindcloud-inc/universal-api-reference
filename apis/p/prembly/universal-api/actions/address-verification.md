# Prembly: Address Verification

Creates an address verification in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/address-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/address-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/address-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "addressStatus": "string",
      "agreedToTermsOfUse": true,
      "city": "string",
      "consented": true,
      "createdAt": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "identity_number": "string",
      "identity_type": "string",
      "isIDNumberVerified": true,
      "isReportReady": true,
      "job_id": "string",
      "last_name": "Chen",
      "lga": "string",
      "phone": "string",
      "requestingCompany": "string",
      "state": "string",
      "street": "string",
      "updatedAt": 1,
      "verificationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `addressStatus` | string |  |
| `agreedToTermsOfUse` | boolean |  |
| `city` | string |  |
| `consented` | boolean |  |
| `createdAt` | number |  |
| `email` | string |  |
| `first_name` | string |  |
| `identity_number` | string |  |
| `identity_type` | string |  |
| `isIDNumberVerified` | boolean |  |
| `isReportReady` | boolean |  |
| `job_id` | string |  |
| `last_name` | string |  |
| `lga` | string |  |
| `phone` | string |  |
| `requestingCompany` | string |  |
| `state` | string |  |
| `street` | string |  |
| `updatedAt` | number |  |
| `verificationType` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/address` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/address-verification.md) for the provider-specific parameters and requirements.

