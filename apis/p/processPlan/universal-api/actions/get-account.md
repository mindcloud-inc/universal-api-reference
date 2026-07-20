# Process Plan: Get Account



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-account?${params}`, {
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
      "account_obj": {
        "acc_allow_proxy_management": true,
        "acc_auto_submit_email_responses": true,
        "acc_billing_country_code": "string",
        "acc_created_date_local": "2026-05-07T12:00:00.000Z",
        "acc_date_format": 1,
        "acc_id": "string",
        "acc_name": "Ava Chen",
        "acc_public_user_ug_id": "string",
        "acc_robot_ug_id": "string",
        "acc_status": "string",
        "acc_ui_bar_color": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_obj.acc_allow_proxy_management` | boolean |  |
| `account_obj.acc_auto_submit_email_responses` | boolean |  |
| `account_obj.acc_billing_country_code` | string |  |
| `account_obj.acc_created_date_local` | date |  |
| `account_obj.acc_date_format` | number |  |
| `account_obj.acc_id` | string |  |
| `account_obj.acc_name` | string |  |
| `account_obj.acc_public_user_ug_id` | string |  |
| `account_obj.acc_robot_ug_id` | string |  |
| `account_obj.acc_status` | string |  |
| `account_obj.acc_ui_bar_color` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /account` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

