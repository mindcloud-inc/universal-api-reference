# Bigjpg: Get Task Result

Retrieves task results from Bigjpg by task ID.

```
GET https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigjpg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result?connectionId=$CONNECTION_ID&taskIds=tid1%2Ctid2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskIds": "tid1,tid2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result?${params}`, {
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
| `taskIds` | string | yes | One or more Bigjpg task IDs, comma-separated in the request path. Accepts multiple values in one string, delimited by `,`. Example: `tid1,tid2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Task processing status from Bigjpg. |
| `url` | string | Result image URL when Bigjpg has completed the task. |

## Native endpoint

Through the native Bigjpg API, this operation is `GET /task/:taskIds` (base URL `https://bigjpg.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-result.md) for the provider-specific parameters and requirements.

