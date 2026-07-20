# Time Doctor: Get Authorization

Retrieves authorization details from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-authorization?${params}`, {
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
      "active": true,
      "adminSettings": {},
      "companies": [
        {}
      ],
      "email": "ava@example.com",
      "emailConfirmed": true,
      "id": "string",
      "lastSeenGlobal": {},
      "lastTrackGlobal": {},
      "name": "Ava Chen",
      "timezones": "string",
      "twoFactorAuth": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `adminSettings` | object |  |
| `companies` | array<object> |  |
| `email` | string |  |
| `emailConfirmed` | boolean |  |
| `id` | string |  |
| `lastSeenGlobal` | object |  |
| `lastTrackGlobal` | object |  |
| `name` | string |  |
| `timezones` | string |  |
| `twoFactorAuth` | boolean |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/authorization` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorization.md) for the provider-specific parameters and requirements.

