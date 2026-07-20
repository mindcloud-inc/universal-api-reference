# Cloudmersive: Get Top-Level Domain From URL

Retrieves a top-level domain from a URL in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-top-level-domain-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-top-level-domain-from-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-top-level-domain-from-url?${params}`, {
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
| `URL` | string | no | URL to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "topLevelDomainName": "Ava Chen",
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
| `topLevelDomainName` | string |  |
| `validUrl` | boolean |  |
| `wellFormedUrl` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/domain/url/get-top-level-domain` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-level-domain-from-url.md) for the provider-specific parameters and requirements.

