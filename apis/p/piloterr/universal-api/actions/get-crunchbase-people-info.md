# Piloterr: Get Crunchbase People Info



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-people-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-people-info?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-crunchbase-people-info?${params}`, {
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
| `query` | string | yes | Crunchbase person slug, name, or URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPositions": {
        "title": "string"
      },
      "name": "Ava Chen",
      "permalink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPositions.title` | string |  |
| `name` | string |  |
| `permalink` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /crunchbase/people/info` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crunchbase-people-info.md) for the provider-specific parameters and requirements.

