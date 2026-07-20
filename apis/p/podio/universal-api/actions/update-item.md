# Podio: Update Item

Updates an existing item in Podio.

```
PUT https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "123456789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | number | yes | The id of the item. Example: `123456789`. |
| `fields` | object | no | Field values keyed by field id or external id. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hook` | boolean | no | True to run item hooks. |
| `silent` | boolean | no | True to suppress notifications. |
| `revision` | number | no | Revision to update from when resolving concurrent edits. Example: `1`. |
| `externalId` | string | no | Unique external id for the item. Example: `external-item-001`. |
| `fileIds[]` | array<number> | no | Files to attach to the item. Example: `12345`. |
| `tags[]` | array<string> | no | Tags to add to the item. Example: `priority`. |
| `reminder` | object | no | Reminder configuration for the item. |
| `recurrence` | object | no | Recurrence settings for the item. |
| `linkedAccountId` | number | no | Linked account id to use when updating the item. Example: `12345`. |
| `ref` | object | no | Reference object used for ratings or app auth. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revision": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revision` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Podio API, this operation is `PUT /item/:item_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

