# PiAPI/Toolkit: PiAPI Account Info

Retrieves account details from PiAPI/Toolkit.

```
GET https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/piapi-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Toolkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/piapi-account-info?${params}`, {
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
      "account_group": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit_pack_info": {
        "available_credits": 1,
        "credit_packs_count": 1,
        "credit_packs": [
          {
            "active": true,
            "capacity": 1,
            "expired_at": "2026-05-07T12:00:00.000Z",
            "id": 1
          }
        ],
        "total_credits": 1
      },
      "equivalent_in_usd": 1,
      "id": 1,
      "is_enable": true,
      "is_using_private_chat_gpt_pool": true,
      "is_using_private_kling_pool": true,
      "is_using_private_luma_pool": true,
      "is_using_private_suno_pool": true,
      "is_using_private_udio_pool": true,
      "is_verified": true,
      "max_concurrent_task_count": 1,
      "max_image_toolkit_concurrency": 1,
      "name": "Ava Chen",
      "notification_hook_url": "https://example.com",
      "plan": "string",
      "platform": "string",
      "private_chat_gpt_pool_size": 1,
      "private_hailuo_pool_size": 1,
      "private_kling_pool_size": 1,
      "private_luma_pool_size": 1,
      "private_pool_size": 1,
      "private_suno_pool_size": 1,
      "private_udio_pool_size": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "wallet": {
        "auto_recharge_enabled": true,
        "gpts_remain": 1,
        "id": 1,
        "llm_remain": 1,
        "llm_used": 1,
        "luma_remain": 1,
        "mj_remain": 1,
        "point_frozen": 1,
        "point_remain": 1,
        "point_used": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_group` | string |  |
| `created_at` | date |  |
| `credit_pack_info.available_credits` | number |  |
| `credit_pack_info.credit_packs_count` | number |  |
| `credit_pack_info.credit_packs[].active` | boolean |  |
| `credit_pack_info.credit_packs[].capacity` | number |  |
| `credit_pack_info.credit_packs[].expired_at` | date |  |
| `credit_pack_info.credit_packs[].id` | number |  |
| `credit_pack_info.total_credits` | number |  |
| `equivalent_in_usd` | number |  |
| `id` | number |  |
| `is_enable` | boolean |  |
| `is_using_private_chat_gpt_pool` | boolean |  |
| `is_using_private_kling_pool` | boolean |  |
| `is_using_private_luma_pool` | boolean |  |
| `is_using_private_suno_pool` | boolean |  |
| `is_using_private_udio_pool` | boolean |  |
| `is_verified` | boolean |  |
| `max_concurrent_task_count` | number |  |
| `max_image_toolkit_concurrency` | number |  |
| `name` | string |  |
| `notification_hook_url` | string |  |
| `plan` | string |  |
| `platform` | string |  |
| `private_chat_gpt_pool_size` | number |  |
| `private_hailuo_pool_size` | number |  |
| `private_kling_pool_size` | number |  |
| `private_luma_pool_size` | number |  |
| `private_pool_size` | number |  |
| `private_suno_pool_size` | number |  |
| `private_udio_pool_size` | number |  |
| `type` | string |  |
| `updated_at` | date |  |
| `wallet.auto_recharge_enabled` | boolean |  |
| `wallet.gpts_remain` | number |  |
| `wallet.id` | number |  |
| `wallet.llm_remain` | number |  |
| `wallet.llm_used` | number |  |
| `wallet.luma_remain` | number |  |
| `wallet.mj_remain` | number |  |
| `wallet.point_frozen` | number |  |
| `wallet.point_remain` | number |  |
| `wallet.point_used` | number |  |

## Native endpoint

Through the native PiAPI/Toolkit API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/piapi-account-info.md) for the provider-specific parameters and requirements.

