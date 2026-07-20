# Scrapeless: Update Browser Extension

Updates an existing browser extension in Scrapeless.

```
PUT https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-browser-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-browser-extension" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extensionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/update-browser-extension', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extensionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensionId` | string | extension id |
| `name` | string | extension name |

## Native endpoint

Through the native Scrapeless API, this operation is `PUT /browser/extensions/:extensionId` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-browser-extension.md) for the provider-specific parameters and requirements.

