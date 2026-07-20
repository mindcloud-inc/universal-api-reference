# CodeQR - Link and QR Analytics: Delete Domain

Deletes a domain from CodeQR.

```
DELETE https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-domain?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-domain?${params}`, {
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
| `slug` | string | yes | The domain name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `slug` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `DELETE /domains/:slug` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-domain.md) for the provider-specific parameters and requirements.

