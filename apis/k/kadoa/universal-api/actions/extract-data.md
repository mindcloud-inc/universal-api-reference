# Kadoa: Extract Data



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/extract-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/extract-data?connectionId=$CONNECTION_ID&link=https%3A%2F%2Fexample.com&schemaId=markdown" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "link": "https://example.com",
  "schemaId": "markdown"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/extract-data?${params}`, {
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
| `link` | string | yes | URL to extract from Default: `https://example.com`. |
| `schemaId` | string | yes | Schema ID or: html, body, markdown Default: `markdown`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "link": "https://example.com",
      "location": {
        "type": "string"
      },
      "requestTimeMs": 1,
      "screenshotUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `link` | string |  |
| `location.type` | string |  |
| `requestTimeMs` | number |  |
| `screenshotUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Kadoa API, this operation is `POST /v4/adhoc/:schemaId` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data.md) for the provider-specific parameters and requirements.

