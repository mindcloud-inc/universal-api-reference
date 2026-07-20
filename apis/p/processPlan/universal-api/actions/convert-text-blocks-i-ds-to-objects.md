# Process Plan: Convert Text Blocks IDs to Objects



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-text-blocks-i-ds-to-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-text-blocks-i-ds-to-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-text-blocks-i-ds-to-objects?${params}`, {
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
      "text_block_list": [
        {
          "tb_acc_id": "string",
          "tb_created_date_local": "2026-05-07T12:00:00.000Z",
          "tb_created_usr_id": "string",
          "tb_html": "string",
          "tb_id": "string",
          "tb_modified_date_local": "2026-05-07T12:00:00.000Z",
          "tb_modified_usr_id": "string",
          "tb_name": "Ava Chen"
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
| `text_block_list[].tb_acc_id` | string |  |
| `text_block_list[].tb_created_date_local` | date |  |
| `text_block_list[].tb_created_usr_id` | string |  |
| `text_block_list[].tb_html` | string |  |
| `text_block_list[].tb_id` | string |  |
| `text_block_list[].tb_modified_date_local` | date |  |
| `text_block_list[].tb_modified_usr_id` | string |  |
| `text_block_list[].tb_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `POST /text_block/id_list/to_object/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-blocks-i-ds-to-objects.md) for the provider-specific parameters and requirements.

