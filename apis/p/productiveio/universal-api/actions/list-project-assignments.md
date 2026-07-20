# Productive.io: List Project Assignments

Retrieves project assignments from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-project-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-project-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-project-assignments?${params}`, {
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
| `personId` | string | no | Filter project assignments by person ID. |
| `projectId` | string | no | Filter project assignments by project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "budgetsFilterId": 1,
        "createdAt": "string",
        "dealsFilterId": 1,
        "defaultFilterId": 1,
        "docsFilterId": 1,
        "invoicesFilterId": 1,
        "preferences": "string",
        "tasksLayoutId": 1,
        "watched": true
      },
      "id": "string",
      "relationships": {
        "budgetsFavoriteFilter": {
          "meta": {
            "included": true
          }
        },
        "dealsFavoriteFilter": {
          "meta": {
            "included": true
          }
        },
        "docsFavoriteFilter": {
          "meta": {
            "included": true
          }
        },
        "favoriteFilter": {
          "meta": {
            "included": true
          }
        },
        "invoicesFavoriteFilter": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "person": {
          "meta": {
            "included": true
          }
        },
        "project": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.budgetsFilterId` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.dealsFilterId` | number |  |
| `attributes.defaultFilterId` | number |  |
| `attributes.docsFilterId` | number |  |
| `attributes.invoicesFilterId` | number |  |
| `attributes.preferences` | string |  |
| `attributes.tasksLayoutId` | number |  |
| `attributes.watched` | boolean |  |
| `id` | string |  |
| `relationships.budgetsFavoriteFilter.meta.included` | boolean |  |
| `relationships.dealsFavoriteFilter.meta.included` | boolean |  |
| `relationships.docsFavoriteFilter.meta.included` | boolean |  |
| `relationships.favoriteFilter.meta.included` | boolean |  |
| `relationships.invoicesFavoriteFilter.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.person.meta.included` | boolean |  |
| `relationships.project.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /project_assignments` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-assignments.md) for the provider-specific parameters and requirements.

