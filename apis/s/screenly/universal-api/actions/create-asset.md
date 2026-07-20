# Screenly: Create Asset

Creates a new asset in Screenly.

```
POST https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenly/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disableVerification` | boolean | no |  |
| `folderName` | string | no |  |
| `jsInjection` | string | no |  |
| `sourceUrl` | string | yes |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetUrl": "https://example.com",
      "disableVerification": true,
      "duration": 1,
      "finalized": true,
      "height": 1,
      "id": "string",
      "md5": "string",
      "metadata": {},
      "sourceMd5": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetUrl` | string |  |
| `disableVerification` | boolean |  |
| `duration` | number |  |
| `finalized` | boolean |  |
| `height` | number |  |
| `id` | string |  |
| `md5` | string |  |
| `metadata` | object |  |
| `sourceMd5` | string |  |
| `sourceUrl` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Screenly API, this operation is `POST /assets/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset.md) for the provider-specific parameters and requirements.

