# Process Plan: List Audit Entries for Proxy Job



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-audit-entries-for-proxy-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-audit-entries-for-proxy-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-audit-entries-for-proxy-job?${params}`, {
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
| `proxyJobId` | string | no | Proxy job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audit_entry_list": [
        {
          "aud_context_usr_id": "string",
          "aud_created_date_local": "2026-05-07T12:00:00.000Z",
          "aud_created_usr_id": "string",
          "aud_created_usr_obj": {
            "usr_email_address": "ava@example.com",
            "usr_first_name": "Ava",
            "usr_full_name": "Ava Chen",
            "usr_id": "string",
            "usr_last_name": "Chen",
            "usr_profile_pic_url": "https://example.com"
          },
          "aud_description": "string",
          "aud_id": "string",
          "aud_updated_field": "string",
          "aud_updated_table": "string",
          "aud_updated_value_new": "2026-05-07T12:00:00.000Z",
          "aud_updated_value_old": "2026-05-07T12:00:00.000Z"
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
| `audit_entry_list[].aud_context_usr_id` | string |  |
| `audit_entry_list[].aud_created_date_local` | date |  |
| `audit_entry_list[].aud_created_usr_id` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_email_address` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_first_name` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_full_name` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_id` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_last_name` | string |  |
| `audit_entry_list[].aud_created_usr_obj.usr_profile_pic_url` | string |  |
| `audit_entry_list[].aud_description` | string |  |
| `audit_entry_list[].aud_id` | string |  |
| `audit_entry_list[].aud_updated_field` | string |  |
| `audit_entry_list[].aud_updated_table` | string |  |
| `audit_entry_list[].aud_updated_value_new` | date |  |
| `audit_entry_list[].aud_updated_value_old` | date |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /proxy_job/:proxyJobId/audit_entry/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audit-entries-for-proxy-job.md) for the provider-specific parameters and requirements.

