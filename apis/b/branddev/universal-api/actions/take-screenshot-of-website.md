# Brand.dev: Take Screenshot of Website

Retrieves a website screenshot from Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/take-screenshot-of-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/take-screenshot-of-website?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/take-screenshot-of-website?${params}`, {
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
| `domain` | string | yes | Domain name to take a screenshot of. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "domain": "string",
      "screenshot": "string",
      "screenshotType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `domain` | string |  |
| `screenshot` | string |  |
| `screenshotType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /brand/screenshot` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/take-screenshot-of-website.md) for the provider-specific parameters and requirements.

