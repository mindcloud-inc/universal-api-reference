# PrintNode: List Print Job States by Set

Retrieves print job states for specific jobs from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states-by-set?connectionId=$CONNECTION_ID&printJobSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "printJobSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states-by-set?${params}`, {
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
| `printJobSet` | string | yes | Comma-separated PrintNode print job IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": 1,
      "clientVersion": "string",
      "createTimestamp": "2026-05-07T12:00:00.000Z",
      "data": {},
      "message": "string",
      "printJobId": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | number | Milliseconds elapsed since the print job entered the new state. |
| `clientVersion` | string | Client version that reported the state when present. |
| `createTimestamp` | date | Timestamp when the state entry was created. |
| `data` | object | Reserved PrintNode payload for future state details. |
| `message` | string | Additional state message when present. |
| `printJobId` | number | Print job identifier for the state entry. |
| `state` | string | PrintNode state token. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /printjobs/:printJobSet/states` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-print-job-states-by-set.md) for the provider-specific parameters and requirements.

