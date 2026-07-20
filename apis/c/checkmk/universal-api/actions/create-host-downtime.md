# Checkmk: Create Host Downtime

Creates a host-related scheduled downtime in Checkmk.

```
POST https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-host-downtime
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-host-downtime" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostName": "Ava Chen",
  "comment": "string",
  "startTime": "2026-05-07T12:00:00.000Z",
  "endTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-host-downtime', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostName": "Ava Chen",
    "comment": "string",
    "startTime": "2026-05-07T12:00:00.000Z",
    "endTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostName` | string | yes | Host to schedule downtime for. |
| `comment` | string | yes | Downtime comment. |
| `startTime` | date | yes | Downtime start time. |
| `endTime` | date | yes | Downtime end time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `POST /domain-types/downtime/collections/host` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-host-downtime.md) for the provider-specific parameters and requirements.

