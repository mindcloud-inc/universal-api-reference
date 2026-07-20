# NextDNS: Get Parental Control

Retrieves parental control settings for a NextDNS profile.

```
GET https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-parental-control
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-parental-control?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-parental-control?${params}`, {
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
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockBypass": true,
      "categories": [
        {}
      ],
      "recreation": {},
      "safeSearch": true,
      "services": [
        {}
      ],
      "youtubeRestrictedMode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockBypass` | boolean |  |
| `categories` | array<object> |  |
| `recreation` | object |  |
| `safeSearch` | boolean |  |
| `services` | array<object> |  |
| `youtubeRestrictedMode` | boolean |  |

## Native endpoint

Through the native NextDNS API, this operation is `GET /profiles/:profile/parentalControl` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parental-control.md) for the provider-specific parameters and requirements.

