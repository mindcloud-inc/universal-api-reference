# updown.io: Get Check

Retrieves a monitoring check from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/get-check?${params}`, {
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
| `metrics` | boolean | no | Include performance metrics from the last hour. |
| `token` | string | yes | The check unique token. |

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
      "domain": {},
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
| `apdex_t` | number | APDEX threshold. |
| `created_at` | date | Creation timestamp. |
| `custom_headers` | object | Custom request headers. |
| `disabled_locations` | array<string> | Disabled locations. |
| `domain` | object | Domain metadata. |
| `down` | boolean | Whether the check is currently down. |
| `down_since` | date | When the check most recently went down. |
| `enabled` | boolean | Whether the check is enabled. |
| `error` | string | Last error message. |
| `favicon_url` | string | Favicon URL. |
| `http_body` | string | Configured request body. |
| `http_verb` | string | HTTP method configuration. |
| `last_check_at` | date | Last check timestamp. |
| `last_status` | number | Last HTTP status code. |
| `mute_until` | date | Mute-until timestamp. |
| `next_check_at` | date | Next check timestamp. |
| `period` | number | Check interval in seconds. |
| `published` | boolean | Whether the check is published. |
| `recipients` | array<string> | Recipient identifiers. |
| `string_match` | string | Expected string match. |
| `token` | string | Check token. |
| `type` | string | Check type. |
| `up_since` | date | When the check most recently came back up. |
| `uptime` | number | Current uptime percentage. |
| `url` | string | Monitored URL. |

## Native endpoint

Through the native updown.io API, this operation is `GET /checks/:token` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-check.md) for the provider-specific parameters and requirements.

