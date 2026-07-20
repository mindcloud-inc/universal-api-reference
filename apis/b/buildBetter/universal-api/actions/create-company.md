# BuildBetter: Create Company



```
POST https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Example Corp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Example Corp"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name. Example: `Example Corp`. |
| `domain` | string | no | Company website domain. Example: `example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | Company color value. Example: `#3366FF`. |
| `photoUrl` | string | no | Company logo or photo URL. Example: `https://example.com/logo.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "photo_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Company color value. |
| `domain` | string | Company website domain. |
| `id` | string | BuildBetter company identifier. |
| `name` | string | Company name. |
| `photo_url` | string | Company logo or photo URL. |
| `updated_at` | date | Last updated timestamp. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

