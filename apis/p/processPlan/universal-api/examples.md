# Process Plan Universal API Examples

These examples use the MindCloud API key and Process Plan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Process Instance Field



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-field?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "process_instance_field_obj": {
        "if_acc_id": "string",
        "if_created_date_local": "2026-05-07T12:00:00.000Z",
        "if_created_usr_id": "string",
        "if_id": "string",
        "if_ih_id": "string",
        "if_modified_date_local": "2026-05-07T12:00:00.000Z",
        "if_modified_usr_id": "string",
        "if_postback_on_change": true,
        "if_text": "string",
        "if_tf_id": "string",
        "if_tf_obj": {
          "tf_id": "string",
          "tf_name": "Ava Chen",
          "tf_required": true,
          "tf_type": 1
        },
        "if_th_id": "string",
        "if_ui_hide": true,
        "if_ui_read_only": true,
        "if_ui_required": true,
        "if_value": "string",
        "if_value_numeric": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Process Instance Field action reference](actions/get-process-instance-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/processPlan/latest/actions/get-process-instance-field).

## Apply File for Message



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/apply-file-for-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/apply-file-for-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Apply File for Message action reference](actions/apply-file-for-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/processPlan/latest/actions/apply-file-for-message).
