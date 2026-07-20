# Trackabi: List Members

Retrieves company members from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-members?${params}`, {
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
      "": [
        {
          "address": "string",
          "avatar": "string",
          "billableRate": {
            "amount": "string",
            "currency": "string"
          },
          "birthdate": "string",
          "education": "string",
          "email": "ava@example.com",
          "emergencyContact": "string",
          "emergencyPhone": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "leaveAllowance": 1,
          "notes": "string",
          "payRate": {
            "amount": "string",
            "currency": "string"
          },
          "personalEmail": "ava@example.com",
          "phone": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].address` | string |  |
| `[].avatar` | string |  |
| `[].billableRate.amount` | string |  |
| `[].billableRate.currency` | string |  |
| `[].birthdate` | string |  |
| `[].education` | string |  |
| `[].email` | string |  |
| `[].emergencyContact` | string |  |
| `[].emergencyPhone` | string |  |
| `[].firstName` | string |  |
| `[].id` | number |  |
| `[].lastName` | string |  |
| `[].leaveAllowance` | number |  |
| `[].notes` | string |  |
| `[].payRate.amount` | string |  |
| `[].payRate.currency` | string |  |
| `[].personalEmail` | string |  |
| `[].phone` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/members` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

