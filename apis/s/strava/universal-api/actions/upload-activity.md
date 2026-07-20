# Strava: Upload Activity

Creates a new activity upload in Strava.

```
POST https://connect.mindcloud.co/v1/universal/strava/latest/actions/upload-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strava `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strava/latest/actions/upload-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "dataType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strava/latest/actions/upload-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "dataType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The activity file content or file reference. |
| `dataType` | string | yes | The uploaded file format such as fit, tcx, or gpx. |
| `name` | string | no | Optional activity name. |
| `description` | string | no | Optional activity description. |
| `externalId` | string | no | An external identifier for de-duplication. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Strava API returns.

## Native endpoint

Through the native Strava API, this operation is `POST /uploads` (base URL `https://www.strava.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-activity.md) for the provider-specific parameters and requirements.

