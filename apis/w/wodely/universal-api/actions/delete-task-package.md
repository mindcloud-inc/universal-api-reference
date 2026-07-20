# Wodely: Delete Task Package



```
DELETE https://connect.mindcloud.co/v1/universal/wodely/latest/actions/delete-task-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/delete-task-package?connectionId=$CONNECTION_ID&packageId=12345&taskGuid=your-task-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "12345",
  "taskGuid": "your-task-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wodely/latest/actions/delete-task-package?${params}`, {
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
| `packageId` | number | yes | Package identifier returned by Wodely. Example: `12345`. |
| `taskGuid` | string | yes | Task identifier for the package. Example: `your-task-guid`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wodely API returns.

## Native endpoint

Through the native Wodely API, this operation is `DELETE /v2/taskPackages/[:packageId]` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task-package.md) for the provider-specific parameters and requirements.

