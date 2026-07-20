# Doctly: Delete Extractor



```
DELETE https://connect.mindcloud.co/v1/universal/doctly/latest/actions/delete-extractor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/delete-extractor?connectionId=$CONNECTION_ID&extractorId=987fcdeb-a654-3210-9876-543210987654" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractorId": "987fcdeb-a654-3210-9876-543210987654"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doctly/latest/actions/delete-extractor?${params}`, {
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
| `extractorId` | string | yes | Unique extractor UUID to delete. Example: `987fcdeb-a654-3210-9876-543210987654`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Doctly API returns.

## Native endpoint

Through the native Doctly API, this operation is `DELETE /e/:extractorId` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-extractor.md) for the provider-specific parameters and requirements.

