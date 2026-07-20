# Intelliprint: Create Background



```
POST https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-background
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-background', {
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
| `file` | file | yes | Base64 string or file URL for the background artwork. |
| `name` | string | no | Optional background name. |
| `team` | string | no | Optional team ID to scope the background. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "created": 1,
      "file": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `created` | number |  |
| `file` | object |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `pdf` | string |  |

## Native endpoint

Through the native Intelliprint API, this operation is `POST /backgrounds` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-background.md) for the provider-specific parameters and requirements.

