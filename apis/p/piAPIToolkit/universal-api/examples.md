# PiAPI/Toolkit Universal API Examples

These examples use the MindCloud API key and PiAPI/Toolkit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## PiAPI Account Info

Retrieves account details from PiAPI/Toolkit.

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

Example response:

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

See the full [PiAPI Account Info action reference](actions/piapi-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIToolkit/latest/actions/piapi-account-info).

## File Upload API

Uploads a file for PiAPI/Toolkit tasks.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/file-upload-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/file-upload-api', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileData": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [File Upload API action reference](actions/file-upload-api.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIToolkit/latest/actions/file-upload-api).
