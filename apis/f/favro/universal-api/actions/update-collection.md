# Favro: Update Collection

Updates an existing collection in Favro.

```
PUT https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/update-collection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | The Favro collection ID to update. |
| `name` | string | yes | The new collection name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "background": "string",
      "collectionId": "string",
      "fullMembersCanAddWidgets": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "publicSharing": "string",
      "sharedToUsers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `background` | string |  |
| `collectionId` | string |  |
| `fullMembersCanAddWidgets` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `publicSharing` | string |  |
| `sharedToUsers` | array<object> |  |

## Native endpoint

Through the native Favro API, this operation is `PUT /collections/:collectionId` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection.md) for the provider-specific parameters and requirements.

