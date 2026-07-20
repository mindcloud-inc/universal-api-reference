# ApproveThis: Delete Template

Deletes an approval template from ApproveThis by slug.

```
DELETE https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/delete-template?connectionId=$CONNECTION_ID&template=mindcloud-template-probe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template": "mindcloud-template-probe"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/delete-template?${params}`, {
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
| `template` | string | yes | The template slug. Example: `mindcloud-template-probe`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ApproveThis API returns.

## Native endpoint

Through the native ApproveThis API, this operation is `DELETE /templates/:template` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

