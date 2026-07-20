# Favro: Create Collection

Creates a new collection in Favro.

```
POST https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Favro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-collection', {
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
| `name` | string | yes | The name of the collection to create. |

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

Through the native Favro API, this operation is `POST /collections` (base URL `https://favro.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

