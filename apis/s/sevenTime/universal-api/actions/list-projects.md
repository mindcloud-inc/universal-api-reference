# Seven Time: List Projects

Retrieves projects from a Seven Time workspace.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-projects?${params}`, {
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
| `name` | string | no | Filter projects by name. |
| `projectNumber` | string | no | Filter projects by project number. |
| `lastModified` | date | no | Include projects modified since the given timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingMethod": "string",
      "estimatedTime": 1,
      "fixedPrice": 1,
      "fixedPriceInvoiced": true,
      "fixedPriceLeftToInvoice": 1,
      "Id": "string",
      "name": "Ava Chen",
      "permissions": {},
      "pricePerHour": 1,
      "projectNumber": "string",
      "projectStatus": 1,
      "projectStatusRef": "string",
      "projectType": "string",
      "projectTypeName": "Ava Chen",
      "recurringBudget": {},
      "recurringBudgetType": 1,
      "tags": [
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
| `billingMethod` | string |  |
| `estimatedTime` | number |  |
| `fixedPrice` | number |  |
| `fixedPriceInvoiced` | boolean |  |
| `fixedPriceLeftToInvoice` | number |  |
| `Id` | string |  |
| `name` | string |  |
| `permissions` | object |  |
| `pricePerHour` | number |  |
| `projectNumber` | string |  |
| `projectStatus` | number |  |
| `projectStatusRef` | string |  |
| `projectType` | string |  |
| `projectTypeName` | string |  |
| `recurringBudget` | object |  |
| `recurringBudgetType` | number |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /projects` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

