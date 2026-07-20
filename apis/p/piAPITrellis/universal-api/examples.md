# PiAPI/Trellis Universal API Examples

These examples use the MindCloud API key and PiAPI/Trellis connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your account information from PiAPI/Trellis.

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

Example response:

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

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPITrellis/latest/actions/get-account-info).

## Create Trellis Image-to-3D Task

Creates a Trellis image-to-3D task in PiAPI/Trellis.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-image-to-3d-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.images[]": "https://upload.wikimedia.org/wikipedia/commons/3/3a/Cat03.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPITrellis/latest/actions/create-trellis-image-to-3d-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.images[]": "https://upload.wikimedia.org/wikipedia/commons/3/3a/Cat03.jpg"
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

See the full [Create Trellis Image-to-3D Task action reference](actions/create-trellis-image-to-3d-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPITrellis/latest/actions/create-trellis-image-to-3d-task).
