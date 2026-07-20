# CodeQR - Link and QR Analytics: Get Link

Retrieves a link from CodeQR.

```
GET https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/get-link?connectionId=$CONNECTION_ID&projectSlug=string&domain=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectSlug": "string",
  "domain": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/get-link?${params}`, {
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
| `projectSlug` | string | yes | The slug of the project to which the link belongs. |
| `domain` | string | yes | The domain of the link to retrieve. |
| `key` | string | yes | The key of the link to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "clicks": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "externalId": "string",
      "id": "string",
      "key": "string",
      "shortLink": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `clicks` | number |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `key` | string |  |
| `shortLink` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `GET /links/info` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

