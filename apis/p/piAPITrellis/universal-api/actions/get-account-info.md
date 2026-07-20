# PiAPI/Trellis: Get Account Info

Retrieves your account information from PiAPI/Trellis.

```
GET https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Trellis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/get-account-info?${params}`, {
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
      "account_mj_bot_group_relations": [
        {}
      ],
      "account_mj_worker_node_group_relations": [
        {}
      ],
      "account_tags": [
        "string"
      ],
      "api_key": "string",
      "auto_challenge_mj_verification": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit_pack_info": {},
      "equivalent_in_usd": 1,
      "id": 1,
      "is_enable": true,
      "is_using_private_chat_gpt_pool": true,
      "is_using_private_kling_pool": true,
      "is_using_private_luma_pool": true,
      "is_using_private_suno_pool": true,
      "is_using_private_udio_pool": true,
      "is_verified": true,
      "kling_failover_enabled": true,
      "luma_failover_enabled": true,
      "max_concurrent_task_count": 1,
      "max_flux_concurrency": 1,
      "max_hailuo_concurrency": 1,
      "max_image_toolkit_concurrency": 1,
      "max_internal_proxy_concurrency": 1,
      "max_kling_concurrency": 1,
      "max_luma_concurrency": 1,
      "max_suno_concurrency": 1,
      "max_trellis_concurrency": 1,
      "max_udio_concurrency": 1,
      "mj_failover_enabled": true,
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
      "skip_suno_flagged_account": true,
      "suno_failover_enabled": true,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "wallet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_group` | string |  |
| `account_mj_bot_group_relations` | array<object> |  |
| `account_mj_worker_node_group_relations` | array<object> |  |
| `account_tags` | array |  |
| `api_key` | string |  |
| `auto_challenge_mj_verification` | boolean |  |
| `created_at` | date |  |
| `credit_pack_info` | object |  |
| `equivalent_in_usd` | number |  |
| `id` | number |  |
| `is_enable` | boolean |  |
| `is_using_private_chat_gpt_pool` | boolean |  |
| `is_using_private_kling_pool` | boolean |  |
| `is_using_private_luma_pool` | boolean |  |
| `is_using_private_suno_pool` | boolean |  |
| `is_using_private_udio_pool` | boolean |  |
| `is_verified` | boolean |  |
| `kling_failover_enabled` | boolean |  |
| `luma_failover_enabled` | boolean |  |
| `max_concurrent_task_count` | number |  |
| `max_flux_concurrency` | number |  |
| `max_hailuo_concurrency` | number |  |
| `max_image_toolkit_concurrency` | number |  |
| `max_internal_proxy_concurrency` | number |  |
| `max_kling_concurrency` | number |  |
| `max_luma_concurrency` | number |  |
| `max_suno_concurrency` | number |  |
| `max_trellis_concurrency` | number |  |
| `max_udio_concurrency` | number |  |
| `mj_failover_enabled` | boolean |  |
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
| `skip_suno_flagged_account` | boolean |  |
| `suno_failover_enabled` | boolean |  |
| `type` | string |  |
| `updated_at` | date |  |
| `wallet` | object |  |

## Native endpoint

Through the native PiAPI/Trellis API, this operation is `GET /account/info` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

