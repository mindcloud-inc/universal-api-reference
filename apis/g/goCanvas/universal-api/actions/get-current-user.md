# GoCanvas: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/get-current-user?${params}`, {
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
      "companyId": 1,
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": "string",
      "defaultDepartmentId": 1,
      "defaultDepartmentName": "Ava Chen",
      "defaultDepartmentRole": "string",
      "enabled": true,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "login": "string",
      "phone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `defaultDepartmentId` | number |  |
| `defaultDepartmentName` | string |  |
| `defaultDepartmentRole` | string |  |
| `enabled` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `login` | string |  |
| `phone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /me` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

