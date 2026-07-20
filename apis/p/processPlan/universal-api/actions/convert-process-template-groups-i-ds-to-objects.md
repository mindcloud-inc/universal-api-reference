# Process Plan: Convert Process Template Groups IDs to Objects



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-process-template-groups-i-ds-to-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-process-template-groups-i-ds-to-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/convert-process-template-groups-i-ds-to-objects?${params}`, {
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
      "process_template_group_list": [
        {
          "pg_acc_id": "string",
          "pg_created_date_local": "2026-05-07T12:00:00.000Z",
          "pg_created_usr_id": "string",
          "pg_icon_name": "Ava Chen",
          "pg_id": "string",
          "pg_modified_date_local": "2026-05-07T12:00:00.000Z",
          "pg_modified_usr_id": "string",
          "pg_name": "Ava Chen"
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
| `process_template_group_list[].pg_acc_id` | string |  |
| `process_template_group_list[].pg_created_date_local` | date |  |
| `process_template_group_list[].pg_created_usr_id` | string |  |
| `process_template_group_list[].pg_icon_name` | string |  |
| `process_template_group_list[].pg_id` | string |  |
| `process_template_group_list[].pg_modified_date_local` | date |  |
| `process_template_group_list[].pg_modified_usr_id` | string |  |
| `process_template_group_list[].pg_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `POST /process_template_group/id_list/to_object/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-process-template-groups-i-ds-to-objects.md) for the provider-specific parameters and requirements.

