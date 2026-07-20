# Webflow: Create Items

Creates staged collection items in Webflow.

```
POST https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "items": {},
  "items[].fieldData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "items": {},
    "items[].fieldData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | The unique identifier of the collection. |
| `items` | list<object> | yes | List of collection items to create. |
| `items[].fieldData` | object | yes | Field data payload for each item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isArchived` | boolean | no | Set created items as archived. |
| `isDraft` | boolean | no | Set created items as draft. |
| `cmsLocaleIds` | list<string> | no | Locales to apply when creating localized items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> | Created collection items. |

## Native endpoint

Through the native Webflow API, this operation is `POST /collections/:collection_id/items` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-items.md) for the provider-specific parameters and requirements.

