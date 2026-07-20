# Time Doctor: Get User Totals

Retrieves user totals from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-totals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-user-totals?${params}`, {
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
      "adminsCount": 1,
      "managersCount": 1,
      "regularUsersCount": 1,
      "totalUsers": 1,
      "usersWithBlurScreenshotsEnabled": 1,
      "usersWithEditTimeEnabled": 1,
      "usersWithScreenshotsEnabled": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminsCount` | number |  |
| `managersCount` | number |  |
| `regularUsersCount` | number |  |
| `totalUsers` | number |  |
| `usersWithBlurScreenshotsEnabled` | number |  |
| `usersWithEditTimeEnabled` | number |  |
| `usersWithScreenshotsEnabled` | number |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/users/totals` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-totals.md) for the provider-specific parameters and requirements.

