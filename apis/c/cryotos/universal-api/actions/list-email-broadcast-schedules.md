# Cryotos: List Email Broadcast Schedules



```
GET https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-email-broadcast-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryotos `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-email-broadcast-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/list-email-broadcast-schedules?${params}`, {
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
      "creationDate": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "updationDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `creationDate` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `updationDate` | string |  |

## Native endpoint

Through the native Cryotos API, this operation is `GET /api/email-broadcast-schedule` (base URL `https://app.cryotos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-broadcast-schedules.md) for the provider-specific parameters and requirements.

