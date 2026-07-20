# Hoversignal: Delete Signal Hook



```
DELETE https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/delete-signal-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/delete-signal-hook?connectionId=$CONNECTION_ID&hookId=00000000-0000-0000-0000-000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hookId": "00000000-0000-0000-0000-000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/delete-signal-hook?${params}`, {
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
| `hookId` | string | yes | Hook identifier. Default: `00000000-0000-0000-0000-000000000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the operation completed successfully. |

## Native endpoint

Through the native Hoversignal API, this operation is `DELETE /api/v1/hooks/{hookId}` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-signal-hook.md) for the provider-specific parameters and requirements.

