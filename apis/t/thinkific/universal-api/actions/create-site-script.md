# Thinkific: Create Site Script

Creates a new site script in Thinkific.

```
POST https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-site-script
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-site-script" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "description": "string",
  "name": "Ava Chen",
  "pageScopes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-site-script', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "description": "string",
    "name": "Ava Chen",
    "pageScopes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | Site script category. |
| `content` | string | no | Inline script content (use either content or src). |
| `description` | string | yes | Site script description. |
| `loadMethod` | string | no | Script load method. |
| `location` | string | no | Injection location for the script. |
| `name` | string | yes | Site script name. |
| `pageScopes[]` | array<string> | yes | Pages and domains where the script should be injected. |
| `src` | string | no | External script source URL (use either src or content). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "content": "string",
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "loadMethod": "string",
      "location": "string",
      "name": "Ava Chen",
      "pageScopes": [
        "string"
      ],
      "src": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `content` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `loadMethod` | string |  |
| `location` | string |  |
| `name` | string |  |
| `pageScopes` | array<string> |  |
| `src` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Thinkific API, this operation is `POST /site_scripts` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site-script.md) for the provider-specific parameters and requirements.

