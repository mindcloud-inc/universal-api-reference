# Cloudmersive: Validate URL Fully

Validates a URL fully in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-url-fully
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-url-fully?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-url-fully?${params}`, {
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
| `URL` | string | no | URL to validate fully. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "validDomain": true,
      "validEndpoint": true,
      "validSyntax": true,
      "validUrl": true,
      "wellFormedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `validDomain` | boolean |  |
| `validEndpoint` | boolean |  |
| `validSyntax` | boolean |  |
| `validUrl` | boolean |  |
| `wellFormedUrl` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/domain/url/full` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-url-fully.md) for the provider-specific parameters and requirements.

