# Moxie: Search Projects

Finds projects in Moxie.

```
GET https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moxie/latest/actions/search-projects?${params}`, {
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
| `query` | string | no | Optional client name filter if you only want projects for a specific client. Example: `Moxie, Inc.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "active": true,
      "clientId": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "feeSchedule": {
        "amount": 1,
        "estimateMax": 1,
        "estimateMin": 1,
        "feeType": "string",
        "retainerActive": true,
        "retainerSchedule": "string",
        "retainerTiming": "string",
        "taxable": true,
        "updatedBy": "string",
        "updatedDate": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "leadGenArchived": true,
      "name": "Ava Chen",
      "portalAccess": "string",
      "portalAccessAssignedOnly": true,
      "projectTypeId": "string",
      "sampleData": true,
      "showTimeWorkedInPortal": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `active` | boolean |  |
| `clientId` | string |  |
| `dateCreated` | date |  |
| `dueDate` | date |  |
| `feeSchedule.amount` | number |  |
| `feeSchedule.estimateMax` | number |  |
| `feeSchedule.estimateMin` | number |  |
| `feeSchedule.feeType` | string |  |
| `feeSchedule.retainerActive` | boolean |  |
| `feeSchedule.retainerSchedule` | string |  |
| `feeSchedule.retainerTiming` | string |  |
| `feeSchedule.taxable` | boolean |  |
| `feeSchedule.updatedBy` | string |  |
| `feeSchedule.updatedDate` | date |  |
| `id` | string |  |
| `leadGenArchived` | boolean |  |
| `name` | string |  |
| `portalAccess` | string |  |
| `portalAccessAssignedOnly` | boolean |  |
| `projectTypeId` | string |  |
| `sampleData` | boolean |  |
| `showTimeWorkedInPortal` | boolean |  |

## Native endpoint

Through the native Moxie API, this operation is `GET /action/projects/search` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.

