# Centerpoint: List Work Time Entries



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-work-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-work-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-work-time-entries?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[workTimeEntries]` | string | no | Feilds: lunchBreakMinutes,inAt,outAt On-Demand Fields: active_hours |
| `fields[profiles]` | string | no |  |
| `fields[employees]` | string | no |  |
| `fields[productions]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "confirmedAt": {},
        "costCode": {},
        "createdAt": "string",
        "deletedAt": {},
        "hours": 1,
        "inAt": "string",
        "isOvertime": true,
        "isTimekeeping": true,
        "localInAtDate": "string",
        "localInAtTime": "string",
        "localOutAtDate": "string",
        "localOutAtTime": "string",
        "lunchBreakMinutes": 1,
        "managerId": {},
        "options": {
          "perDiem": true
        },
        "outAt": "string",
        "productionId": {},
        "profileId": 1,
        "rate": 1,
        "timezone": "string",
        "type": {},
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.confirmedAt` | object |  |
| `attributes.costCode` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.hours` | number |  |
| `attributes.inAt` | string |  |
| `attributes.isOvertime` | boolean |  |
| `attributes.isTimekeeping` | boolean |  |
| `attributes.localInAtDate` | string |  |
| `attributes.localInAtTime` | string |  |
| `attributes.localOutAtDate` | string |  |
| `attributes.localOutAtTime` | string |  |
| `attributes.lunchBreakMinutes` | number |  |
| `attributes.managerId` | object |  |
| `attributes.options.perDiem` | boolean |  |
| `attributes.outAt` | string |  |
| `attributes.productionId` | object |  |
| `attributes.profileId` | number |  |
| `attributes.rate` | number |  |
| `attributes.timezone` | string |  |
| `attributes.type` | object |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET work_time_entries` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-time-entries.md) for the provider-specific parameters and requirements.

