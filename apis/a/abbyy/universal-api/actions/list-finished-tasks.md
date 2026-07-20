# Abbyy: List Finished Tasks

Retrieves finished OCR tasks from ABBYY Cloud OCR SDK.

```
GET https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-finished-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abbyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-finished-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/list-finished-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abbyy API returns.

## Native endpoint

Through the native Abbyy API, this operation is `GET /v2/listFinishedTasks` (base URL `https://cloud-westus.ocrsdk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-finished-tasks.md) for the provider-specific parameters and requirements.

