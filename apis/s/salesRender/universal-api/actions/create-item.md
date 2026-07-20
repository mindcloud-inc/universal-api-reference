# SalesRender: Create Item

Creates a new item in SalesRender.

```
POST https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CreateItem($input: AddItemInput!) {\n  itemMutation {\n    addItem(input: $input) {\n      id\n      name\n      units\n      archived\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/create-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CreateItem($input: AddItemInput!) {\n  itemMutation {\n    addItem(input: $input) {\n      id\n      name\n      units\n      archived\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object. Set `input` to a valid AddItemInput payload. Default: `{"input":{}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation to execute. Default: `mutation CreateItem($input: AddItemInput!) {\n  itemMutation {\n    addItem(input: $input) {\n      id\n      name\n      units\n      archived\n    }\n  }\n}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "itemMutation": {
          "addItem": {
            "archived": true,
            "id": "string",
            "name": "Ava Chen",
            "units": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.itemMutation.addItem.archived` | boolean |  |
| `data.itemMutation.addItem.id` | string |  |
| `data.itemMutation.addItem.name` | string |  |
| `data.itemMutation.addItem.units` | string |  |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item.md) for the provider-specific parameters and requirements.

