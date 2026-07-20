# Linkila: Get Access Log

Retrieves access log entries from Linkila.

```
GET https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-access-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-access-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/get-access-log?${params}`, {
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
| `before` | date | no | Optional ISO date-time cursor; return access-log entries before this timestamp. |
| `limit` | number | no | Maximum number of access-log entries to return. Official maximum: 500. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Optional Linkila analytics filter object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "pageInfo": {},
        "results": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Access-log response object. |
| `data.pageInfo` | object | Access-log pagination metadata including lastTs. |
| `data.results` | array<object> | Access log entries with timestamp, linkId, shortURLId, ip, ref_url, region, language, deviceType, os_name, browser_name. |

## Native endpoint

Through the native Linkila API, this operation is `POST /analytics/accessLog` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-log.md) for the provider-specific parameters and requirements.

