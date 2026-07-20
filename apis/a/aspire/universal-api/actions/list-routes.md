# Aspire: List Routes



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-routes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-routes?${params}`, {
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
      "allowEquipmentTimeReporting": true,
      "branchID": 1,
      "branchName": "Ava Chen",
      "color": "string",
      "crewLeaderContactID": 1,
      "crewLeaderContactName": "Ava Chen",
      "displayOrder": 1,
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "equipmentID": {},
      "equipmentName": {},
      "hours": 1,
      "managerContactID": 1,
      "managerName": "Ava Chen",
      "percentTravelTime": 1,
      "routeID": 1,
      "routeName": "Ava Chen",
      "routeSize": 1,
      "showDailyPlan": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allowEquipmentTimeReporting` | boolean |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `color` | string |  |
| `crewLeaderContactID` | number |  |
| `crewLeaderContactName` | string |  |
| `displayOrder` | number |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `equipmentID` | object |  |
| `equipmentName` | object |  |
| `hours` | number |  |
| `managerContactID` | number |  |
| `managerName` | string |  |
| `percentTravelTime` | number |  |
| `routeID` | number |  |
| `routeName` | string |  |
| `routeSize` | number |  |
| `showDailyPlan` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Routes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-routes.md) for the provider-specific parameters and requirements.

