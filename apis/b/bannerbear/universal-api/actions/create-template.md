# Bannerbear: Create Template

Creates a new template in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "width": 1,
    "height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the new blank template. |
| `width` | number | yes | The width of the new blank template. |
| `height` | number | yes | The height of the new blank template. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | no | Custom metadata to store with the template. |
| `tags[]` | array<string> | no | An array of tags for the template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/templates` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

