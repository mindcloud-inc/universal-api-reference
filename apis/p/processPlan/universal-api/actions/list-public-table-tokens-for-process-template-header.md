# Process Plan: List Public Table Tokens for Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-public-table-tokens-for-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-public-table-tokens-for-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-public-table-tokens-for-process-template-header?${params}`, {
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
| `processTemplateHeaderId` | string | no | Process template header ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token_obj": {
        "tkn_acc_id": "string",
        "tkn_expire_date_local": "2026-05-07T12:00:00.000Z",
        "tkn_id": "string",
        "tkn_running_in_background_job": true,
        "tkn_type": 1,
        "tkn_usr_id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token_obj.tkn_acc_id` | string |  |
| `token_obj.tkn_expire_date_local` | date |  |
| `token_obj.tkn_id` | string |  |
| `token_obj.tkn_running_in_background_job` | boolean |  |
| `token_obj.tkn_type` | number |  |
| `token_obj.tkn_usr_id` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/public_table_token/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-public-table-tokens-for-process-template-header.md) for the provider-specific parameters and requirements.

