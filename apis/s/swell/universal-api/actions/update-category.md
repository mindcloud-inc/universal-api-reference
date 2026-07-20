# Swell: Update Category



```
PUT https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Swell category ID. |
| `name` | string | no | The category name. |
| `active` | boolean | no | Whether the category is active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `dateCreated` | date |  |
| `id` | string |  |
| `name` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native Swell API, this operation is `PUT /categories/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

