# Todoist: Create Label

Creates a new label in Todoist.

```
POST https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Label name. |
| `order` | number | no | Custom label order value. |
| `color` | string | no | Label color name or legacy color code. Default: `charcoal`. |
| `isFavorite` | boolean | no | Whether the label should be marked as favorite. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "isFavorite": true,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Label color |
| `id` | string | Label ID |
| `isFavorite` | boolean | Whether label is favorite |
| `name` | string | Label name |
| `order` | number | Label sort order |

## Native endpoint

Through the native Todoist API, this operation is `POST /api/v1/labels` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-label.md) for the provider-specific parameters and requirements.

