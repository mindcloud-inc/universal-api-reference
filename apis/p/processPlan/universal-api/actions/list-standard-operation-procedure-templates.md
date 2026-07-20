# Process Plan: List Standard Operation Procedure Templates



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-standard-operation-procedure-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-standard-operation-procedure-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-standard-operation-procedure-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result_list": [
        {
          "developer_message": "string",
          "message_number": 1,
          "user_message": "string"
        }
      ],
      "sop_template_list": [
        {
          "sop_acc_id": "string",
          "sop_created_date_local": "2026-05-07T12:00:00.000Z",
          "sop_created_usr_id": "string",
          "sop_html": "string",
          "sop_id": "string",
          "sop_modified_date_local": "2026-05-07T12:00:00.000Z",
          "sop_modified_usr_id": "string",
          "sop_name": "Ava Chen"
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
| `result_list[].developer_message` | string |  |
| `result_list[].message_number` | number |  |
| `result_list[].user_message` | string |  |
| `sop_template_list[].sop_acc_id` | string |  |
| `sop_template_list[].sop_created_date_local` | date |  |
| `sop_template_list[].sop_created_usr_id` | string |  |
| `sop_template_list[].sop_html` | string |  |
| `sop_template_list[].sop_id` | string |  |
| `sop_template_list[].sop_modified_date_local` | date |  |
| `sop_template_list[].sop_modified_usr_id` | string |  |
| `sop_template_list[].sop_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /sop_template/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-standard-operation-procedure-templates.md) for the provider-specific parameters and requirements.

