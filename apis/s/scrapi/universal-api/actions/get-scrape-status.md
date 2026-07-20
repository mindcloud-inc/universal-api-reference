# Scrapi: Get Scrape Status

Retrieves a Scrapi scrape status by callback reference.

```
GET https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-scrape-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-scrape-status?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/get-scrape-status?${params}`, {
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
| `reference` | string | yes | Callback reference to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reference": "string",
      "status": "string",
      "text": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reference` | string |  |
| `status` | string |  |
| `text` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Scrapi API, this operation is `GET /v1/scrape/status/{reference}` (base URL `https://api.scrapi.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scrape-status.md) for the provider-specific parameters and requirements.

