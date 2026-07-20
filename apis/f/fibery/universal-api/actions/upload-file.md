# Fibery: Upload File

Creates a new file in Fibery.

```
POST https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes |  |

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

Through the native Fibery API, this operation is `POST /files` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

