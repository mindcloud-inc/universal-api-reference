# Routee: Get shorten URL info for monitoring purposes

Retrieves shortened URL monitoring details from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-shorten-url-info-for-monitoring-purposes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-shorten-url-info-for-monitoring-purposes?connectionId=$CONNECTION_ID&%7BtrackingId%7D=string&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "{trackingId}": "string",
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-shorten-url-info-for-monitoring-purposes?${params}`, {
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
| `{trackingId}` | string | yes | The unique traking id of a shorten URL |
| `trackingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "createdAt": "string",
      "expirationDate": "string",
      "link": "https://example.com",
      "longUrl": "https://example.com",
      "name": "Ava Chen",
      "tags": {
        "tag1": "string",
        "tag2": "string"
      },
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `createdAt` | string |  |
| `expirationDate` | string |  |
| `link` | string |  |
| `longUrl` | string |  |
| `name` | string |  |
| `tags` | object |  |
| `tags.tag1` | string |  |
| `tags.tag2` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /shorten/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shorten-url-info-for-monitoring-purposes.md) for the provider-specific parameters and requirements.

