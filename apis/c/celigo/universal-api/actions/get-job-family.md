# Celigo: Get Job Family



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-job-family
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-job-family?connectionId=$CONNECTION_ID&jobId=6798e7a330f8f5fb4c2ee2fb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "6798e7a330f8f5fb4c2ee2fb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-job-family?${params}`, {
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
| `jobId` | string | yes | Job ID, typically a parent flow-run job. Returns the job with its child step jobs under children. Example: `6798e7a330f8f5fb4c2ee2fb`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Celigo API returns.

## Native endpoint

Through the native Celigo API, this operation is `GET /jobs/:jobId/family` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-family.md) for the provider-specific parameters and requirements.

