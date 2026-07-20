# Zoho Assist: Get User Info

Gets details for the current Zoho Assist user.

```
GET https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info?${params}`, {
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
      "departments": [
        {}
      ],
      "joinDomain": "string",
      "license": {},
      "multiOrgEnabled": true,
      "nightModeEnabled": true,
      "orgDetails": {},
      "preferredDepartment": "string",
      "role": {},
      "screenName": "Ava Chen",
      "userRole": 1,
      "zuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departments` | array<object> |  |
| `joinDomain` | string |  |
| `license` | object |  |
| `multiOrgEnabled` | boolean |  |
| `nightModeEnabled` | boolean |  |
| `orgDetails` | object |  |
| `preferredDepartment` | string |  |
| `role` | object |  |
| `screenName` | string |  |
| `userRole` | number |  |
| `zuid` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `GET /user` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

