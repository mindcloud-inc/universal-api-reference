# Process Plan: Get Text Block



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-text-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-text-block?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-text-block?${params}`, {
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
| `textBlockId` | string | no | Text block ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tb_acc_id` | string |  |
| `tb_created_date_local` | date |  |
| `tb_created_usr_id` | string |  |
| `tb_html` | string |  |
| `tb_id` | string |  |
| `tb_modified_date_local` | date |  |
| `tb_modified_usr_id` | string |  |
| `tb_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /text_block/:textBlockId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-text-block.md) for the provider-specific parameters and requirements.

