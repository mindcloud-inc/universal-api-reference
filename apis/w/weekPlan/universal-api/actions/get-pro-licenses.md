# Week Plan: Get Pro Licenses



```
GET https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-pro-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-pro-licenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-pro-licenses?${params}`, {
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
      "CreatedAt": "string",
      "Email": "ava@example.com",
      "ExpiresAt": "string",
      "LicenseId": 1,
      "UserId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedAt` | string |  |
| `Email` | string |  |
| `ExpiresAt` | string |  |
| `LicenseId` | number |  |
| `UserId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `GET users/pro_licenses` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pro-licenses.md) for the provider-specific parameters and requirements.

