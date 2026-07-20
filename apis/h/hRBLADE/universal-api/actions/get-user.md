# HRBLADE: Get User



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user?${params}`, {
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
      "code": 1,
      "error": true,
      "response": {
        "data": {
          "agency": {
            "aiRequestsCount": 1,
            "aiRequestsLimit": 1,
            "clientType": "string",
            "companiesLimit": 1,
            "countryCode": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": 1,
            "interviewsLimit": 1,
            "planId": 1,
            "quantity": 1,
            "responsesLimit": 1,
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "usersLimit": 1,
            "videoDefinition": "string"
          },
          "country": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": 1,
          "lang": "string",
          "name": "Ava Chen",
          "recruitingOwner": 1,
          "role": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        },
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | boolean |  |
| `response.data.agency.aiRequestsCount` | number |  |
| `response.data.agency.aiRequestsLimit` | number |  |
| `response.data.agency.clientType` | string |  |
| `response.data.agency.companiesLimit` | number |  |
| `response.data.agency.countryCode` | string |  |
| `response.data.agency.createdAt` | date |  |
| `response.data.agency.id` | number |  |
| `response.data.agency.interviewsLimit` | number |  |
| `response.data.agency.planId` | number |  |
| `response.data.agency.quantity` | number |  |
| `response.data.agency.responsesLimit` | number |  |
| `response.data.agency.updatedAt` | date |  |
| `response.data.agency.usersLimit` | number |  |
| `response.data.agency.videoDefinition` | string |  |
| `response.data.country` | string |  |
| `response.data.createdAt` | date |  |
| `response.data.email` | string |  |
| `response.data.id` | number |  |
| `response.data.lang` | string |  |
| `response.data.name` | string |  |
| `response.data.recruitingOwner` | number |  |
| `response.data.role` | string |  |
| `response.data.updatedAt` | date |  |
| `response.message` | string |  |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /user` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

