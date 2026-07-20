# Process Plan: Get Process Template Group



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-group?${params}`, {
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
| `processTemplateGroupId` | string | no | Process template group ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pg_acc_id` | string |  |
| `pg_created_date_local` | date |  |
| `pg_created_usr_id` | string |  |
| `pg_icon_name` | string |  |
| `pg_id` | string |  |
| `pg_modified_date_local` | date |  |
| `pg_modified_usr_id` | string |  |
| `pg_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_group/:processTemplateGroupId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process-template-group.md) for the provider-specific parameters and requirements.

