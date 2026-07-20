# Basin: Delete Submission

Deletes an existing submission from Basin.

```
DELETE https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-submission?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-submission?${params}`, {
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
| `id` | number | yes | ID of the submission to destroy. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basin API returns.

## Native endpoint

Through the native Basin API, this operation is `DELETE /api/v1/submissions/:id` (base URL `https://usebasin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-submission.md) for the provider-specific parameters and requirements.

