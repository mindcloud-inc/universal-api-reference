# Prerender.io: List Events History

Retrieves event history from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-events-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-events-history?connectionId=$CONNECTION_ID&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-events-history?${params}`, {
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
| `domain` | string | no |  |
| `events` | string | no |  |
| `from` | string | yes |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `sort` | string | no |  |
| `sortDirection` | string | no |  |
| `to` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/events-history` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-events-history.md) for the provider-specific parameters and requirements.

