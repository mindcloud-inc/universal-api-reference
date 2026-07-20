# Ritekit: Get Company Logo

Retrieves a company logo from Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-logo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-logo?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-logo?${params}`, {
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
| `domain` | string | yes | Company domain to fetch a logo for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandColors": [
        "string"
      ],
      "code": 1,
      "domain": "string",
      "isGenerated": true,
      "message": "string",
      "originalLogo": {},
      "permanentUrl": "https://example.com",
      "result": true,
      "squareLogo": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandColors` | array<string> |  |
| `code` | number |  |
| `domain` | string |  |
| `isGenerated` | boolean |  |
| `message` | string |  |
| `originalLogo` | object |  |
| `permanentUrl` | string |  |
| `result` | boolean |  |
| `squareLogo` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/company-insights/logo` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-logo.md) for the provider-specific parameters and requirements.

