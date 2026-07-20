# Samply: Disable Player Downloads (Tenant-Limited)



```
PUT https://connect.mindcloud.co/v1/universal/samply/latest/actions/disable-player-downloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/samply/latest/actions/disable-player-downloads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samply/latest/actions/disable-player-downloads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `playerid` | string | no | The Samply player id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "options": {},
      "projectid": "string",
      "public": true,
      "timeCreated": 1,
      "timeModified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `options` | object |  |
| `projectid` | string |  |
| `public` | boolean |  |
| `timeCreated` | number |  |
| `timeModified` | number |  |

## Native endpoint

Through the native Samply API, this operation is `POST /players/:playerid` (base URL `https://samply.app/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-player-downloads.md) for the provider-specific parameters and requirements.

