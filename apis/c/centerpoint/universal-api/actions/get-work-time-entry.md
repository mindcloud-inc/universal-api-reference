# Centerpoint: Get Work Time Entry



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-work-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-work-time-entry?connectionId=$CONNECTION_ID&WORK_TIME_ENTRIES_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "WORK_TIME_ENTRIES_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-work-time-entry?${params}`, {
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
| `WORK_TIME_ENTRIES_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[employees]` | string | no |  |
| `fields[profiles]` | string | no |  |
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

Through the native Centerpoint API, this operation is `GET work_time_entries/:WORK_TIME_ENTRIES_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-time-entry.md) for the provider-specific parameters and requirements.

