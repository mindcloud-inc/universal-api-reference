# Statsig: Create Assignment Source

Creates an assignment source in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-assignment-source-post-console-v1-experiments-assignment-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-assignment-source-post-console-v1-experiments-assignment-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sql": "string",
  "timestampColumn": "string",
  "experimentIDColumn": "string",
  "groupIDColumn": "string",
  "idTypeMapping": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-assignment-source-post-console-v1-experiments-assignment-sources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sql": "string",
    "timestampColumn": "string",
    "experimentIDColumn": "string",
    "groupIDColumn": "string",
    "idTypeMapping": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Request body field. |
| `description` | string | no | Request body field. |
| `isVerified` | boolean | no | Request body field. |
| `tags` | list | no | Request body field. |
| `sql` | string | yes | Request body field. |
| `timestampColumn` | string | yes | Request body field. |
| `experimentIDColumn` | string | yes | Request body field. |
| `groupIDColumn` | string | yes | Request body field. |
| `groupNameColumn` | string | no | Request body field. |
| `idTypeMapping` | list | yes | Request body field. |
| `isReadOnly` | boolean | no | Request body field. |
| `owner` | object | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `scheduledReloadHour` | number | no | Request body field. |
| `dryRun` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/experiments/assignment_sources` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assignment-source-post-console-v1-experiments-assignment-sources.md) for the provider-specific parameters and requirements.

