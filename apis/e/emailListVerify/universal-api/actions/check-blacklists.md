# EmailListVerify: Check Blacklists

Checks IP or domain blacklists in EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/check-blacklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/check-blacklists?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/check-blacklists?${params}`, {
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
| `value` | string | yes | IP address or domain to check against DNS-based blacklists. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklists": {
        "description": "string",
        "domain": "https://example.com",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklists` | array<object> | Blacklist providers where the value is listed. |
| `blacklists.description` | string | Listing details or delisting instructions. |
| `blacklists.domain` | string | Blacklist DNS zone. |
| `blacklists.name` | string | Blacklist provider name. |
| `blacklists.url` | string | Provider information URL. |
| `type` | string | Detected value type. |
| `value` | string | Checked IP address or domain. |

## Native endpoint

Through the native EmailListVerify API, this operation is `POST /api/checkBlacklists` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-blacklists.md) for the provider-specific parameters and requirements.

