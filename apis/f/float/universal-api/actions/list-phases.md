# Float: List Phases

Retrieves phases from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-phases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-phases?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "budgetTotal": {},
      "color": {},
      "created": "string",
      "defaultHourlyRate": {},
      "endDate": "string",
      "modified": "string",
      "name": "Ava Chen",
      "nonBillable": {},
      "notes": {},
      "phaseId": 1,
      "projectId": 1,
      "startDate": "string",
      "status": 1,
      "tentative": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `budgetTotal` | object |  |
| `color` | object |  |
| `created` | string |  |
| `defaultHourlyRate` | object |  |
| `endDate` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `nonBillable` | object |  |
| `notes` | object |  |
| `phaseId` | number |  |
| `projectId` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `tentative` | number |  |

## Native endpoint

Through the native Float API, this operation is `GET /phases` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-phases.md) for the provider-specific parameters and requirements.

