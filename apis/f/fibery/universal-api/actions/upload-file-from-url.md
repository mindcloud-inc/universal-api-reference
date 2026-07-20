# Fibery: Upload File From URL

Creates a new file in Fibery from a URL.

```
POST https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Source file URL to upload into Fibery. |
| `name` | string | no | Optional filename to use inside Fibery. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `method` | string | no | HTTP method Fibery should use when downloading the source URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fibery/content-length": 1,
      "fibery/content-type": "string",
      "fibery/id": "string",
      "fibery/name": "Ava Chen",
      "fibery/rank": 1,
      "fibery/secret": "string",
      "fibery/temp?": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fibery/content-length` | number |  |
| `fibery/content-type` | string |  |
| `fibery/id` | string |  |
| `fibery/name` | string |  |
| `fibery/rank` | number |  |
| `fibery/secret` | string |  |
| `fibery/temp?` | boolean |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /files/from-url` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-from-url.md) for the provider-specific parameters and requirements.

