# PrintNode: List Print Job States

Retrieves print job states from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-print-job-states?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native PrintNode API, this operation is `GET /printjobs/states` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-print-job-states.md) for the provider-specific parameters and requirements.

