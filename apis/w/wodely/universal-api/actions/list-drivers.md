# Wodely: List Drivers



```
GET https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/list-drivers?${params}`, {
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
      "address": "string",
      "businessNumber": "string",
      "capacity": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isOnDuty": 1,
      "lastName": "Chen",
      "numActiveTask": 1,
      "phoneNumber": "string",
      "position": "string",
      "profileImage": "string",
      "skills": "string",
      "statusDesc": "string",
      "statusId": 1,
      "teamName": "Ava Chen",
      "telephone": "string",
      "timeZone": "string",
      "transportDesc": "string",
      "transportLicensePlate": "string",
      "transportTypeId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Driver address text. |
| `businessNumber` | string | Business number associated with the driver. |
| `capacity` | number | Driver capacity value. |
| `email` | string | Driver account email address. |
| `firstName` | string | Driver first name. |
| `id` | string | Unique Wodely driver identifier. |
| `isOnDuty` | number | On-duty flag returned by Wodely. |
| `lastName` | string | Driver last name. |
| `numActiveTask` | number | Number of active tasks currently assigned. |
| `phoneNumber` | string | Primary phone number for the driver. |
| `position` | string | Driver position or role label. |
| `profileImage` | string | Profile image filename or reference. |
| `skills` | string | Serialized skills value returned by Wodely. |
| `statusDesc` | string | Driver status label. |
| `statusId` | number | Driver status identifier. |
| `teamName` | string | Team name assigned to the driver. |
| `telephone` | string | Secondary telephone number when available. |
| `timeZone` | string | Driver time zone value. |
| `transportDesc` | string | Transport description. |
| `transportLicensePlate` | string | Transport license plate. |
| `transportTypeId` | number | Transport type identifier. |
| `userName` | string | Username associated with the driver account. |

## Native endpoint

Through the native Wodely API, this operation is `GET /v2/drivers` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-drivers.md) for the provider-specific parameters and requirements.

