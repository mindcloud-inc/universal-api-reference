# Timeular: Create Mention

Creates a new mention in your Timeular workspace.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-mention
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-mention" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "label": "string",
  "scope": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-mention', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "label": "string",
    "scope": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no |  |
| `key` | string | yes |  |
| `label` | string | yes |  |
| `scope` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderId": "string",
      "id": 1,
      "key": "string",
      "label": "string",
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderId` | string |  |
| `id` | number |  |
| `key` | string |  |
| `label` | string |  |
| `scope` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v4/mentions` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mention.md) for the provider-specific parameters and requirements.

