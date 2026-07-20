# Bulldog-WP: Get analytics

Retrieves analytics from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-analytics?connectionId=$CONNECTION_ID&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z&devices=0123456789abcdef01234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z",
  "devices": "0123456789abcdef01234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-analytics?${params}`, {
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
| `from` | date | yes | Start date in ISO 8601 format. |
| `to` | date | yes | End date in ISO 8601 format. |
| `devices` | string<string> | yes | One or more WhatsApp device IDs. Required by the live API for analytics requests. Accepts multiple values in one string, delimited by `,`. Example: `0123456789abcdef01234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compares": [
        {}
      ],
      "metrics": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compares` | array<object> |  |
| `metrics` | array<object> |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /analytics` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics.md) for the provider-specific parameters and requirements.

