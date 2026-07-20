# NeetoCal: Create Scheduling Link

Creates a new scheduling link in NeetoCal.

```
POST https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/create-scheduling-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/create-scheduling-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string",
  "name": "Ava Chen",
  "hosts[]": [
    "string"
  ],
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/create-scheduling-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string",
    "name": "Ava Chen",
    "hosts[]": ["string"],
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Unique slug for the scheduling link. |
| `name` | string | yes | Display name for the scheduling link. |
| `hosts[]` | array<string> | yes | Host emails for the scheduling link. |
| `duration` | number | yes | Duration in minutes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoCal API returns.

## Native endpoint

Through the native NeetoCal API, this operation is `POST /meetings` (base URL `https://{{credentials.subdomain}}.neetocal.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scheduling-link.md) for the provider-specific parameters and requirements.

