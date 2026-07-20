# Process Plan: List Stores for Process Template Headers in Process Template Category



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-stores-for-process-template-headers-in-process-template-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-stores-for-process-template-headers-in-process-template-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-stores-for-process-template-headers-in-process-template-category?${params}`, {
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
| `processTemplateCategoryId` | string | no | Process template category ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_token_list": [
        {
          "display_text": "string",
          "field_token": "string",
          "is_advanced_token": true,
          "is_email_token": true,
          "is_html_token": true,
          "is_multi_row_field": true,
          "is_user_id_token": true
        }
      ],
      "result_list": [
        {
          "developer_message": "string",
          "message_number": 1,
          "user_message": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_token_list[].display_text` | string |  |
| `field_token_list[].field_token` | string |  |
| `field_token_list[].is_advanced_token` | boolean |  |
| `field_token_list[].is_email_token` | boolean |  |
| `field_token_list[].is_html_token` | boolean |  |
| `field_token_list[].is_multi_row_field` | boolean |  |
| `field_token_list[].is_user_id_token` | boolean |  |
| `result_list[].developer_message` | string |  |
| `result_list[].message_number` | number |  |
| `result_list[].user_message` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_category/:processTemplateCategoryId/process_template_header/store/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores-for-process-template-headers-in-process-template-category.md) for the provider-specific parameters and requirements.

