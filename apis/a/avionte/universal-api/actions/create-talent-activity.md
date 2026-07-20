# Avionte: Create Talent Activity



```
POST https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "talentId": "string",
  "notes": "string",
  "activityType": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "talentId": "string",
    "notes": "string",
    "activityType": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `talentId` | string | yes |  |
| `notes` | string | yes |  |
| `name` | string | no |  |
| `activityType` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avionte API returns.

## Native endpoint

Through the native Avionte API, this operation is `POST front-office/v1/talent/:talentId/activity` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-talent-activity.md) for the provider-specific parameters and requirements.

