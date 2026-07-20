# Referral Rock: Delete Hook

Deletes a webhook subscription from Referral Rock.

```
DELETE https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-hook?connectionId=$CONNECTION_ID&webHookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webHookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-hook?${params}`, {
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
| `webHookId` | string | yes | The unique ID of the webhook subscription to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Referral Rock API returns.

## Native endpoint

Through the native Referral Rock API, this operation is `DELETE /api/hooks` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-hook.md) for the provider-specific parameters and requirements.

