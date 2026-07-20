# Veracity Learning: Get More Statements

Retrieves more statements from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-more-statements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-more-statements?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-more-statements?${params}`, {
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
| `id` | string | yes | Opaque continuation id returned by the statements resource |

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

Through the native Veracity Learning API, this operation is `GET /statements/more` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-more-statements.md) for the provider-specific parameters and requirements.

