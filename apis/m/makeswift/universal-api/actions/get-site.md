# Makeswift: Get Site

Retrieves a site from Makeswift.

```
GET https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeswift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-site?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/get-site?${params}`, {
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
| `siteId` | string | yes | The site ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultLocale": "string",
      "hostOrigin": "string",
      "id": "string",
      "localeManagementMode": "string",
      "name": "Ava Chen",
      "object": "string",
      "publicApiKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultLocale` | string |  |
| `hostOrigin` | string |  |
| `id` | string |  |
| `localeManagementMode` | string |  |
| `name` | string |  |
| `object` | string |  |
| `publicApiKey` | string |  |

## Native endpoint

Through the native Makeswift API, this operation is `GET /v2/sites/:siteId` (base URL `https://api.makeswift.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site.md) for the provider-specific parameters and requirements.

