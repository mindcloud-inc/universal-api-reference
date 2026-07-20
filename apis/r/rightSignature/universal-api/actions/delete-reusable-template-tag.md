# RightSignature: Delete Reusable Template Tag

Deletes a tag from a RightSignature reusable template.

```
DELETE https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/delete-reusable-template-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/delete-reusable-template-tag?connectionId=$CONNECTION_ID&tag=string&reusableTemplateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "string",
  "reusableTemplateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/delete-reusable-template-tag?${params}`, {
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
| `tag` | string | yes | Tag name is required |
| `reusableTemplateId` | string | yes | Reusable Template Id value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RightSignature API returns.

## Native endpoint

Through the native RightSignature API, this operation is `DELETE /reusable_templates/:reusable_template_id/tags` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-reusable-template-tag.md) for the provider-specific parameters and requirements.

