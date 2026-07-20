# OTO: Get Account Info

Retrieves account information from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/get-account-info?${params}`, {
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
      "accountType": "string",
      "CRDocStatus": "string",
      "email": "ava@example.com",
      "freelanceDocStatus": "string",
      "mobileNumber": "string",
      "name": "Ava Chen",
      "packageName": "Ava Chen",
      "remainingCredit": 1,
      "remainingFreeShipments": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `CRDocStatus` | string |  |
| `email` | string |  |
| `freelanceDocStatus` | string |  |
| `mobileNumber` | string |  |
| `name` | string |  |
| `packageName` | string |  |
| `remainingCredit` | number |  |
| `remainingFreeShipments` | string |  |

## Native endpoint

Through the native OTO API, this operation is `GET /accountInfo` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

