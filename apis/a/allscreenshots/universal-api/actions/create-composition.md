# Allscreenshots: Create Composition

Creates a single image from multiple screenshots in Allscreenshots.

```
POST https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-composition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-composition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-composition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `captures[]` | array<object> | no | Capture-mode composition input with multiple URLs and optional labels. |
| `url` | string | no | Variants-mode source URL for a composition request. |
| `variants[]` | array<object> | no | Variants-mode device or configuration list. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `output` | object | no | Composition layout and styling options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `POST /v1/screenshots/compose` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-composition.md) for the provider-specific parameters and requirements.

