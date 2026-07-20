# CheckFlow: Get Uploaded Checklist Files



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-uploaded-checklist-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-uploaded-checklist-files?connectionId=$CONNECTION_ID&limit=25&offset=0&taskContentKey=4cb6f84c-950f-4424-aa7b-d12608419d9b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "taskContentKey": "4cb6f84c-950f-4424-aa7b-d12608419d9b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/get-uploaded-checklist-files?${params}`, {
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
| `taskContentKey` | string | yes | The key of the file upload task content control. Example: `4cb6f84c-950f-4424-aa7b-d12608419d9b`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CheckFlow API returns.

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/checklist/uploaded-files` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-uploaded-checklist-files.md) for the provider-specific parameters and requirements.

