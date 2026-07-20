# Weberlo: Create Ad Channel

Creates an ad channel in Weberlo.

```
POST https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-ad-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-ad-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Meta Ads",
  "icon": "https://example.com/ad-channel.png",
  "adPlatform": "facebook",
  "adAccountId": "1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/create-ad-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Meta Ads",
    "icon": "https://example.com/ad-channel.png",
    "adPlatform": "facebook",
    "adAccountId": "1234567890"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Ad channel name. Example: `Meta Ads`. |
| `icon` | string | yes | Ad channel icon URL. Example: `https://example.com/ad-channel.png`. |
| `adPlatform` | string | yes | Ad platform identifier. Example: `facebook`. |
| `adAccountId` | string | yes | Ad account ID. Example: `1234567890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adAccountId": "string",
      "adAccountPlatform": "string",
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adAccountId` | string |  |
| `adAccountPlatform` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Weberlo API, this operation is `POST /channel-ad` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ad-channel.md) for the provider-specific parameters and requirements.

