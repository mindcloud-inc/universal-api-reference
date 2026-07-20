# Cloudmersive Security: Check IP Bot Status

Checks an IP address for bot threats in Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status?connectionId=$CONNECTION_ID&ipAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ipAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status?${params}`, {
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
| `ipAddress` | string | yes | IP address to check, for example 55.55.55.55. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsBot": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsBot` | boolean |  |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/network/ip/is-bot` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-ip-bot-status.md) for the provider-specific parameters and requirements.

