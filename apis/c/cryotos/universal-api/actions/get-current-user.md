# Cryotos: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user?${params}`, {
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
      "activated": true,
      "authorities": [
        "string"
      ],
      "communicationEmail": "ava@example.com",
      "companyId": 1,
      "countryCode": "string",
      "dateFormat": "string",
      "dateTimeFormat": "string",
      "designation": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "langKey": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "passwordExpired": true,
      "roleName": "Ava Chen",
      "tenantId": "string",
      "userGroupIds": [
        1
      ],
      "userGroupNames": [
        "Ava Chen"
      ],
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | boolean |  |
| `authorities` | array<string> |  |
| `communicationEmail` | string |  |
| `companyId` | number |  |
| `countryCode` | string |  |
| `dateFormat` | string |  |
| `dateTimeFormat` | string |  |
| `designation` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `langKey` | string |  |
| `lastName` | string |  |
| `mobilePhone` | string |  |
| `passwordExpired` | boolean |  |
| `roleName` | string |  |
| `tenantId` | string |  |
| `userGroupIds` | array<number> |  |
| `userGroupNames` | array<string> |  |
| `workflowType` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/account` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

