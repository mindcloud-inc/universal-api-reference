# Vybit: Get Vybit



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-vybit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-vybit?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-vybit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | The unique key of the vybit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "following": true,
      "geofence": {},
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "message": "string",
      "name": "Ava Chen",
      "numberFollowers": 1,
      "sendPermissions": "string",
      "soundKey": "string",
      "status": "string",
      "subscriptionKey": "string",
      "triggerKey": "string",
      "triggerSettings": {},
      "triggerType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `following` | boolean |  |
| `geofence` | object |  |
| `imageUrl` | string |  |
| `key` | string |  |
| `linkUrl` | string |  |
| `message` | string |  |
| `name` | string |  |
| `numberFollowers` | number |  |
| `sendPermissions` | string |  |
| `soundKey` | string |  |
| `status` | string |  |
| `subscriptionKey` | string |  |
| `triggerKey` | string |  |
| `triggerSettings` | object |  |
| `triggerType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Vybit API, this operation is `GET /vybit/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vybit.md) for the provider-specific parameters and requirements.

