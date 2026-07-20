# Veracity Learning: Get Statement

Retrieves a statement from Veracity Learning by statement ID.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-statement?connectionId=$CONNECTION_ID&statementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-statement?${params}`, {
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
| `statementId` | string | yes | Id of the statement to fetch |
| `format` | string | no | Statement response format: exact, canonical, or ids |
| `attachments` | boolean | no | Include statement attachments in the response |

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

Through the native Veracity Learning API, this operation is `GET /statements` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-statement.md) for the provider-specific parameters and requirements.

