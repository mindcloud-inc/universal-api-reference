# SalesRender: List Items

Retrieves items from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-items?connectionId=$CONNECTION_ID&query=query%20%7B%20itemsFetcher%20%7B%20items%20%7B%20id%20name%20units%20archived%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { itemsFetcher { items { id name units archived } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL query to execute against SalesRender. Default: `query {\n  itemsFetcher {\n    items {\n      id\n      name\n      units\n      archived\n    }\n  }\n}`. Example: `query { itemsFetcher { items { id name units archived } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. Example: `Optional JSON variables string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "itemsFetcher": {
          "items": [
            {
              "archived": true,
              "id": "string",
              "name": "Ava Chen",
              "units": "string"
            }
          ]
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
| `data.itemsFetcher.items[].archived` | boolean | Whether the item is archived. |
| `data.itemsFetcher.items[].id` | string | Item ID. |
| `data.itemsFetcher.items[].name` | string | Item name. |
| `data.itemsFetcher.items[].units` | string | Item units label. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

