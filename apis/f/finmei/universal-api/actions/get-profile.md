# Finmei: Get Profile



```
GET https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/get-profile?${params}`, {
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
      "data": {
        "address": "string",
        "businessId": "string",
        "businessTitle": "string",
        "businessType": "string",
        "companyCode": "string",
        "companyName": "Ava Chen",
        "vatCode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.address` | string |  |
| `data.businessId` | string |  |
| `data.businessTitle` | string |  |
| `data.businessType` | string |  |
| `data.companyCode` | string |  |
| `data.companyName` | string |  |
| `data.vatCode` | string |  |

## Native endpoint

Through the native Finmei API, this operation is `GET /profile` (base URL `https://app.finmei.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

