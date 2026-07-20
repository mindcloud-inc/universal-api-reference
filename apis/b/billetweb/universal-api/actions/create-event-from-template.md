# Billetweb: Create Event From Template

Creates a new event in Billetweb from a template.

```
POST https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/create-event-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/create-event-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/create-event-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Source template event identifier. |
| `name` | string | yes | Name of the new event. |
| `place` | string | no | Location of the new event. |
| `start` | number | no | Event start time as a Unix timestamp. |
| `end` | number | no | Event end time as a Unix timestamp. |
| `cloneDates` | boolean | no | Whether to duplicate the template event sessions. Default: `0`. |
| `cloneLists` | boolean | no | Whether to duplicate related list operations from the template event. Default: `1`. |
| `cloneSeating` | boolean | no | Whether to duplicate numbered seating from the template event. Default: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `POST /event/:id/clone` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-from-template.md) for the provider-specific parameters and requirements.

