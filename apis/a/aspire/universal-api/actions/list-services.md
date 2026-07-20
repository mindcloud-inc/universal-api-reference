# Aspire: List Services



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-services?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allBranches": true,
      "approveTicketOnCompletion": true,
      "contractService": true,
      "defaultPayCodeID": {},
      "defaultPayCodeName": {},
      "displayName": "Ava Chen",
      "equipmentTaxable": true,
      "formID": {},
      "formName": {},
      "laborTaxable": true,
      "materialTaxable": true,
      "minimumPrice": 1,
      "multiVisit": true,
      "otherTaxable": true,
      "serviceDescription": {},
      "serviceID": 1,
      "serviceName": "Ava Chen",
      "serviceNameAbr": "Ava Chen",
      "serviceTypeID": 1,
      "serviceTypeName": "Ava Chen",
      "sortOrder": 1,
      "startFormID": {},
      "subTaxable": true,
      "workersCompID": {},
      "workersCompName": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allBranches` | boolean |  |
| `approveTicketOnCompletion` | boolean |  |
| `contractService` | boolean |  |
| `defaultPayCodeID` | object |  |
| `defaultPayCodeName` | object |  |
| `displayName` | string |  |
| `equipmentTaxable` | boolean |  |
| `formID` | object |  |
| `formName` | object |  |
| `laborTaxable` | boolean |  |
| `materialTaxable` | boolean |  |
| `minimumPrice` | number |  |
| `multiVisit` | boolean |  |
| `otherTaxable` | boolean |  |
| `serviceDescription` | object |  |
| `serviceID` | number |  |
| `serviceName` | string |  |
| `serviceNameAbr` | string |  |
| `serviceTypeID` | number |  |
| `serviceTypeName` | string |  |
| `sortOrder` | number |  |
| `startFormID` | object |  |
| `subTaxable` | boolean |  |
| `workersCompID` | object |  |
| `workersCompName` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Services` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

