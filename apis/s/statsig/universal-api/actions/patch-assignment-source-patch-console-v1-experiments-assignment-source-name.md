# Statsig: Patch Assignment Source

Updates an assignment source in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the assignment source |
| `description` | string | no | Request body field. |
| `isVerified` | boolean | no | Request body field. |
| `tags` | list | no | Request body field. |
| `sql` | string | no | Request body field. |
| `timestampColumn` | string | no | Request body field. |
| `experimentIDColumn` | string | no | Request body field. |
| `groupIDColumn` | string | no | Request body field. |
| `groupNameColumn` | string | no | Request body field. |
| `idTypeMapping` | list | no | Request body field. |
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

Through the native Statsig API, this operation is `PATCH /console/v1/experiments/assignment_source/{name}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-assignment-source-patch-console-v1-experiments-assignment-source-name.md) for the provider-specific parameters and requirements.

