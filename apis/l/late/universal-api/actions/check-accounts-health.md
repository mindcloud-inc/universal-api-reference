# Late: Check Accounts Health



```
GET https://connect.mindcloud.co/v1/universal/late/latest/actions/check-accounts-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/late/latest/actions/check-accounts-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/check-accounts-health?${params}`, {
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
| `profileId` | string | no |  |
| `platform` | list | no | One of: `bluesky`, `facebook`, `googlebusiness`, `instagram`, `linkedin`, `pinterest`, `reddit`, `snapchat`, `telegram`, `threads`, `tiktok`, `twitter`, `youtube`. |
| `status` | list | no | One of: `error`, `healthy`, `warning`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | Per-account health rows. |
| `summary` | object | Aggregate health summary. |

## Native endpoint

Through the native Late API, this operation is `GET /accounts/health` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-accounts-health.md) for the provider-specific parameters and requirements.

