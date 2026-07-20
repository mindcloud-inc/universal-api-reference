# myUplink: Get My Systems

Retrieves systems for the authenticated myUplink user.

```
GET https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/get-my-systems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a myUplink `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/get-my-systems?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myUplink/latest/actions/get-my-systems?${params}`, {
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
      "country": "string",
      "devices": [
        {}
      ],
      "hasAlarm": true,
      "name": "Ava Chen",
      "securityLevel": "string",
      "systemId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | System country. |
| `devices` | array<object> | Devices linked to the system. |
| `hasAlarm` | boolean | Whether the system currently has an active alarm. |
| `name` | string | System name. |
| `securityLevel` | string | User access level for the system. |
| `systemId` | string | System identifier. |

## Native endpoint

Through the native myUplink API, this operation is `GET /v2/systems/me` (base URL `https://api.myuplink.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-my-systems.md) for the provider-specific parameters and requirements.

