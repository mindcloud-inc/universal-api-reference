# Lettr: Get Template Merge Tags By Version



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template-merge-tags-by-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template-merge-tags-by-version?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template-merge-tags-by-version?${params}`, {
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
| `slug` | string | yes | Template slug. |
| `version` | number | no | Template version number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "merge_tags": {
          "key": "string",
          "required": true
        },
        "project_id": 1,
        "template_slug": "string",
        "version": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Merge tag payload. |
| `data.merge_tags` | array<object> | Merge tags for the template version. |
| `data.merge_tags.key` | string | Merge tag key. |
| `data.merge_tags.required` | boolean | Whether the merge tag is required. |
| `data.project_id` | number | Project ID. |
| `data.template_slug` | string | Template slug. |
| `data.version` | number | Template version number. |
| `message` | string | Merge tag retrieval status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /templates/:slug/merge-tags` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-merge-tags-by-version.md) for the provider-specific parameters and requirements.

