# ApproveThis: List Template Fields

Retrieves fields for an approval template in ApproveThis.

```
GET https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-template-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApproveThis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-template-fields?connectionId=$CONNECTION_ID&template=mindcloud-generated-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template": "mindcloud-generated-template"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-template-fields?${params}`, {
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
| `template` | string | yes | The template slug. Example: `mindcloud-generated-template`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ApproveThis API returns.

## Native endpoint

Through the native ApproveThis API, this operation is `GET /templates/:template/fields` (base URL `https://app.approvethis.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-fields.md) for the provider-specific parameters and requirements.

