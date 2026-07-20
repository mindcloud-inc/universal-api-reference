# Docupilot: Delete Template Merge Link

Deletes a template merge link from Docupilot.

```
DELETE https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/delete-template-merge-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docupilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/delete-template-merge-link?connectionId=$CONNECTION_ID&id=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/delete-template-merge-link?${params}`, {
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
| `id` | string | yes |  |
| `templateId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docupilot API returns.

## Native endpoint

Through the native Docupilot API, this operation is `DELETE /dashboard/api/v2/templates/{template_id}/merge_links/{id}/` (base URL `https://api.docupilot.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template-merge-link.md) for the provider-specific parameters and requirements.

