# Bedrijfsdata.nl: Validate Website URL



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-website-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-website-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/validate-website-url?${params}`, {
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
| `url` | string | no | Website URL to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "product": "string",
      "status": "string",
      "url": {
        "contentLength": 1,
        "contentType": "https://example.com",
        "domain": "https://example.com",
        "httpCode": 1,
        "ip": "https://example.com",
        "redirectCount": 1,
        "success": 1,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |
| `url.contentLength` | number |  |
| `url.contentType` | string |  |
| `url.domain` | string |  |
| `url.httpCode` | number |  |
| `url.ip` | string |  |
| `url.redirectCount` | number |  |
| `url.success` | number |  |
| `url.url` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /url` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-website-url.md) for the provider-specific parameters and requirements.

