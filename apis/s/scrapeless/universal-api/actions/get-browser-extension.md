# Scrapeless: Get Browser Extension

Retrieves a browser extension from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-extension?connectionId=$CONNECTION_ID&extensionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extensionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-extension?${params}`, {
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
| `extensionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensionId": "string",
      "manifestName": "Ava Chen",
      "name": "Ava Chen",
      "teamId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensionId` | string | extension id |
| `manifestName` | string | extension manifest name |
| `name` | string | extension name |
| `teamId` | string | extension team id |
| `version` | string | extension version |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/extensions/:extensionId` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-extension.md) for the provider-specific parameters and requirements.

