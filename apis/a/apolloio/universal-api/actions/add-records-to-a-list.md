# Apollo: Add Records to a List



```
PUT https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/add-records-to-a-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/add-records-to-a-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityIds[]": [
    "string"
  ],
  "labelNames[]": [
    "Ava Chen"
  ],
  "modality": "accounts"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/add-records-to-a-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityIds[]": ["string"],
    "labelNames[]": ["Ava Chen"],
    "modality": "accounts"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityIds[]` | array<string> | yes |  |
| `labelNames[]` | array<string> | yes |  |
| `modality` | list<string> | yes | One of: `accounts`, `contacts`. |
| `async` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cachedCount": 1,
      "createdAt": "string",
      "id": "string",
      "modality": "string",
      "name": "Ava Chen",
      "updatedAt": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cachedCount` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `modality` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/labels/add_entity_ids_to_label_names` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-records-to-a-list.md) for the provider-specific parameters and requirements.

