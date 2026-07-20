# Oneflow: Get Template

Retrieves template details from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | The Oneflow template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "_private": {},
      "attachment_file_groups": [
        {}
      ],
      "available_options": {},
      "configuration": {},
      "created_time": "string",
      "draft_approval_workflow": {},
      "id": 1,
      "name": "Ava Chen",
      "parties": [
        {}
      ],
      "pdf_file_groups": [
        {}
      ],
      "pending_approval_workflow": {},
      "product_groups": [
        {}
      ],
      "sign_order": [
        {}
      ],
      "tags": [
        {}
      ],
      "template_active": true,
      "template_type": {},
      "updated_time": "string",
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `_private` | object |  |
| `attachment_file_groups` | array<object> |  |
| `available_options` | object |  |
| `configuration` | object |  |
| `created_time` | string |  |
| `draft_approval_workflow` | object |  |
| `id` | number |  |
| `name` | string |  |
| `parties` | array<object> |  |
| `pdf_file_groups` | array<object> |  |
| `pending_approval_workflow` | object |  |
| `product_groups` | array<object> |  |
| `sign_order` | array<object> |  |
| `tags` | array<object> |  |
| `template_active` | boolean |  |
| `template_type` | object |  |
| `updated_time` | string |  |
| `workspaces` | array<object> |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /templates/:id` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

