# 123FormBuild: Delete Multiple Forms

Deletes multiple forms from your 123FormBuilder account.

```
DELETE https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-multiple-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-multiple-forms?connectionId=$CONNECTION_ID&formIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/delete-multiple-forms?${params}`, {
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
| `formIds` | string | yes | Comma-separated IDs of the forms to delete |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `DELETE /forms/bulk` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-forms.md) for the provider-specific parameters and requirements.

