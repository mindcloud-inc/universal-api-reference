# Prerender.io: List Domain 404 Check

Retrieves domain 404 checks from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domain-404-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domain-404-check?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-domain-404-check?${params}`, {
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
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": "string",
      "domainCheckSuccess": true,
      "googleIndexedUrlsCount": 1,
      "id": 1,
      "isEnabled": true,
      "lastCheckedAt": "string",
      "randomUrlCheckSuccess": true,
      "revisitInterval": 1,
      "type": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `domain` | string |  |
| `domainCheckSuccess` | boolean |  |
| `googleIndexedUrlsCount` | number |  |
| `id` | number |  |
| `isEnabled` | boolean |  |
| `lastCheckedAt` | string |  |
| `randomUrlCheckSuccess` | boolean |  |
| `revisitInterval` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/domain-404-check` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-domain-404-check.md) for the provider-specific parameters and requirements.

