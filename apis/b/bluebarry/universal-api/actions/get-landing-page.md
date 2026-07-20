# Bluebarry: Get Landing Page

Retrieves a landing page from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-landing-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-landing-page?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-landing-page?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clonedFrom": "string",
      "cloudflareCustomHostnameId": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "customDomain": "string",
      "customDomainVerified": true,
      "faviconUrl": "https://example.com",
      "id": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "name": "Ava Chen",
      "path": "string",
      "reference": "string",
      "sections": [
        {}
      ],
      "seoDescription": "string",
      "seoTitle": "string",
      "status": "string",
      "tenant": "string",
      "tenantId": "string",
      "theme": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clonedFrom` | string |  |
| `cloudflareCustomHostnameId` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `customDomain` | string |  |
| `customDomainVerified` | boolean |  |
| `faviconUrl` | string |  |
| `id` | string |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `name` | string |  |
| `path` | string |  |
| `reference` | string |  |
| `sections` | array<object> |  |
| `seoDescription` | string |  |
| `seoTitle` | string |  |
| `status` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `theme` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `GET /data/LandingPages({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-landing-page.md) for the provider-specific parameters and requirements.

