# RightSignature: Add Or Update Reusable Template Tags

Adds or updates tags on a RightSignature reusable template.

```
PUT https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/add-or-update-reusable-template-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/add-or-update-reusable-template-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags": {},
  "tags.tagName": "Ava Chen",
  "reusableTemplateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/add-or-update-reusable-template-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags": {},
    "tags.tagName": "Ava Chen",
    "reusableTemplateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | list<object> | yes | Optional key value tags for categorization |
| `tags.tagName` | string | yes | Tag name is required |
| `tags.value` | string | no | Optional value for the tag |
| `reusableTemplateId` | string | yes | Reusable Template Id value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RightSignature API returns.

## Native endpoint

Through the native RightSignature API, this operation is `PATCH /reusable_templates/:reusable_template_id/tags` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-reusable-template-tags.md) for the provider-specific parameters and requirements.

