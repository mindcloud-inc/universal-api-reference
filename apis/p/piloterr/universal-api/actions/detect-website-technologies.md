# Piloterr: Detect Website Technologies



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/detect-website-technologies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/detect-website-technologies?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/detect-website-technologies?${params}`, {
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
| `query` | string | yes | Public website URL to analyze for detected technologies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "technologies": {
        "name": "Ava Chen",
        "slug": "string"
      },
      "urls": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `technologies.name` | string |  |
| `technologies.slug` | string |  |
| `urls` | object |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /website/technology` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-website-technologies.md) for the provider-specific parameters and requirements.

