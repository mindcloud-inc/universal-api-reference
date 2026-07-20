# Ellipsend: Create Activity

Creates a new activity in Ellipsend.

```
POST https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "activityTypeId": 1,
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "activityTypeId": 1,
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | The Ellipsend token. |
| `activityTypeId` | number | yes | The activity type ID. |
| `fields` | object | yes | Key/value pairs of fields for the activity. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ellipsend API returns.

## Native endpoint

Through the native Ellipsend API, this operation is `POST https://api.ellipsend.com/v1/activity` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

