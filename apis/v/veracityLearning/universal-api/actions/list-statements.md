# Veracity Learning: List Statements

Retrieves statements from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements?${params}`, {
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
| `agent` | object | no | Filter statements to a specific xAPI Agent JSON object. |
| `verb` | string | no | Filter statements by verb IRI. |
| `activity` | string | no | Filter statements by activity IRI. |
| `registration` | string | no | Filter statements by registration UUID. |
| `since` | date | no | Return statements stored after this timestamp. |
| `until` | date | no | Return statements stored before this timestamp. |
| `format` | string | no | Select the xAPI statement response format. |
| `attachments` | boolean | no | Include attachment content when supported. |
| `ascending` | boolean | no | Return statements in ascending stored order. |
| `relatedActivities` | boolean | no | Include statements related to the supplied activity hierarchy. |
| `relatedAgents` | boolean | no | Include statements related to the supplied agent hierarchy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor": {},
      "authority": {},
      "context": {},
      "id": "string",
      "object": {},
      "result": {},
      "stored": "2026-05-07T12:00:00.000Z",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "verb": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor` | object | Statement actor details |
| `authority` | object | Authority that asserted the statement |
| `context` | object | Statement context metadata |
| `id` | string | Unique xAPI statement identifier |
| `object` | object | Learning activity or target object |
| `result` | object | Statement result payload when present |
| `stored` | date | Timestamp when the LRS stored the statement |
| `timestamp` | date | Original statement timestamp |
| `verb` | object | xAPI verb metadata |

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /statements` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statements.md) for the provider-specific parameters and requirements.

