# SalesRender: List Targets

Retrieves targets from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-targets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-targets?connectionId=$CONNECTION_ID&query=query%20%7B%0A%20%20targetsFetcher%20%7B%0A%20%20%20%20targets%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20name%0A%20%20%20%20%20%20color%0A%20%20%20%20%20%20archived%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query {\n  targetsFetcher {\n    targets {\n      id\n      name\n      color\n      archived\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-targets?${params}`, {
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
| `query` | string | yes | GraphQL query to execute. Default: `query {\n  targetsFetcher {\n    targets {\n      id\n      name\n      color\n      archived\n    }\n  }\n}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object. Default: `{}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "targetsFetcher": {
          "targets": [
            {
              "archived": true,
              "color": "string",
              "id": "string",
              "name": "Ava Chen"
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
| `data.targetsFetcher.targets[].archived` | boolean |  |
| `data.targetsFetcher.targets[].color` | string |  |
| `data.targetsFetcher.targets[].id` | string |  |
| `data.targetsFetcher.targets[].name` | string |  |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-targets.md) for the provider-specific parameters and requirements.

