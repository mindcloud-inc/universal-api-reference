# GoCanvas: Delete Submission Value



```
DELETE https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/delete-submission-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/delete-submission-value?connectionId=$CONNECTION_ID&submissionId=string&valueId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string",
  "valueId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/delete-submission-value?${params}`, {
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
| `submissionId` | string | yes | Numeric ID or mobile GUID of the submission. |
| `valueId` | number | yes | Identifier of the value to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `DELETE /submissions/:submissionId/values/:valueId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-submission-value.md) for the provider-specific parameters and requirements.

