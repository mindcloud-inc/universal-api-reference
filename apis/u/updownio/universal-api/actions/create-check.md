# updown.io: Create Check

Creates a new check in updown.io.

```
POST https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | no | Human-readable name for the check. |
| `apdexT` | number | no | APDEX threshold in seconds. |
| `customHeaders` | object | no | Custom HTTP headers for updown requests. |
| `disabledLocations[]` | array<string> | no | Monitoring locations to disable for this check. |
| `enabled` | boolean | no | Whether the check is enabled. |
| `httpBody` | string | no | HTTP body sent with the request. |
| `httpVerb` | list | no | HTTP verb used for the check request. One of: `DELETE`, `GET/HEAD`, `OPTIONS`, `PATCH`, `POST`, `PUT`. |
| `muteUntil` | string | no | Mute notifications until the given time, recovery, or forever. |
| `period` | number | no | Interval in seconds. |
| `published` | boolean | no | Whether the status page entry is public. |
| `recipients[]` | array<string> | no | Selected alert recipients for the check. |
| `stringMatch` | string | no | Search for this string in the page. |
| `type` | list | no | The type of check to create. One of: `http`, `https`, `icmp`, `pulse`, `tcp`, `tcps`. |
| `url` | string | no | The URL you want to monitor, except for pulse checks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "apdex_t": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_headers": {},
      "disabled_locations": [
        "string"
      ],
      "down": true,
      "down_since": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "error": "string",
      "favicon_url": "https://example.com",
      "http_body": "string",
      "http_verb": "string",
      "last_check_at": "2026-05-07T12:00:00.000Z",
      "last_status": 1,
      "mute_until": "2026-05-07T12:00:00.000Z",
      "next_check_at": "2026-05-07T12:00:00.000Z",
      "period": 1,
      "published": true,
      "recipients": [
        "string"
      ],
      "string_match": "string",
      "token": "string",
      "type": "string",
      "up_since": "2026-05-07T12:00:00.000Z",
      "uptime": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Optional alias. |
| `apdex_t` | number | APDEX threshold in seconds. |
| `created_at` | date | Creation timestamp. |
| `custom_headers` | object | Custom request headers. |
| `disabled_locations` | array<string> | Disabled monitoring locations. |
| `down` | boolean | Whether the check is currently down. |
| `down_since` | date | When the check most recently went down. |
| `enabled` | boolean | Whether the check is enabled. |
| `error` | string | Last error message. |
| `favicon_url` | string | Favicon URL. |
| `http_body` | string | Configured request body. |
| `http_verb` | string | Configured HTTP verb. |
| `last_check_at` | date | Last check timestamp. |
| `last_status` | number | Last HTTP status code. |
| `mute_until` | date | Mute-until timestamp. |
| `next_check_at` | date | Next check timestamp. |
| `period` | number | Check interval in seconds. |
| `published` | boolean | Whether the check is public on a status page. |
| `recipients` | array<string> | Recipient identifiers. |
| `string_match` | string | Expected string match. |
| `token` | string | Check token. |
| `type` | string | Check type. |
| `up_since` | date | When the check most recently came back up. |
| `uptime` | number | Current uptime percentage. |
| `url` | string | Monitored URL. |

## Native endpoint

Through the native updown.io API, this operation is `POST /checks` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-check.md) for the provider-specific parameters and requirements.

