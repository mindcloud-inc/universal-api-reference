# Float: List Time Off

Retrieves time off entries from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off?${params}`, {
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
| `startDate` | string | no | Start of date range in format YYYY-MM-DD |
| `endDate` | string | no | End of date range in format YYYY-MM-DD |
| `fullDay` | number | no | Filter only on whether time off is full day |
| `status` | number | no | Filter on the status of the time off |
| `timeoffTypeId` | number | no | Filter on the ID of the time off type |
| `modifiedSince` | string | no | Filter on records with an equal or later modified timestamp |
| `fields` | string | no | Comma-delimited set of fields to include in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "createdBy": 1,
      "endDate": "string",
      "fullDay": 1,
      "hours": {},
      "modified": "string",
      "modifiedBy": 1,
      "peopleIds": [
        1
      ],
      "repeatEnd": {},
      "repeatState": 1,
      "startDate": "string",
      "startTime": {},
      "status": 1,
      "statusCreatorId": {},
      "statusNote": {},
      "timeoffId": 1,
      "timeoffNotes": "string",
      "timeoffTypeId": 1,
      "timeoffTypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `createdBy` | number |  |
| `endDate` | string |  |
| `fullDay` | number |  |
| `hours` | object |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `peopleIds[]` | number |  |
| `repeatEnd` | object |  |
| `repeatState` | number |  |
| `startDate` | string |  |
| `startTime` | object |  |
| `status` | number |  |
| `statusCreatorId` | object |  |
| `statusNote` | object |  |
| `timeoffId` | number |  |
| `timeoffNotes` | string |  |
| `timeoffTypeId` | number |  |
| `timeoffTypeName` | string |  |

## Native endpoint

Through the native Float API, this operation is `GET /timeoffs` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-off.md) for the provider-specific parameters and requirements.

