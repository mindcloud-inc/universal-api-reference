# Process Plan: List API Tokens for Me



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-api-tokens-for-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-api-tokens-for-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-api-tokens-for-me?${params}`, {
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

Through the native Process Plan API, this operation is `GET /user/me/api_token/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-tokens-for-me.md) for the provider-specific parameters and requirements.

