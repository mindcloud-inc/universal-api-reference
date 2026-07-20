# Aspire: List Activities



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activities?${params}`, {
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
      "activityCategoryID": {},
      "activityCategoryName": {},
      "activityID": 1,
      "activityNumber": {},
      "activityType": "string",
      "completeDate": {},
      "completedByUserID": {},
      "completedByUserName": {},
      "createdByUserID": {},
      "createdByUserName": {},
      "createdDate": "string",
      "dueDate": {},
      "endDate": {},
      "includeClient": true,
      "includeCrew": true,
      "invoiceID": {},
      "isMileStone": true,
      "location": {},
      "modifiedDate": "string",
      "notes": "string",
      "opportunityID": {},
      "paymentID": {},
      "priority": {},
      "private": true,
      "propertyID": {},
      "sentDate": "string",
      "startDate": {},
      "status": {},
      "subject": "string",
      "workTicketID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityCategoryID` | object |  |
| `activityCategoryName` | object |  |
| `activityID` | number |  |
| `activityNumber` | object |  |
| `activityType` | string |  |
| `completeDate` | object |  |
| `completedByUserID` | object |  |
| `completedByUserName` | object |  |
| `createdByUserID` | object |  |
| `createdByUserName` | object |  |
| `createdDate` | string |  |
| `dueDate` | object |  |
| `endDate` | object |  |
| `includeClient` | boolean |  |
| `includeCrew` | boolean |  |
| `invoiceID` | object |  |
| `isMileStone` | boolean |  |
| `location` | object |  |
| `modifiedDate` | string |  |
| `notes` | string |  |
| `opportunityID` | object |  |
| `paymentID` | object |  |
| `priority` | object |  |
| `private` | boolean |  |
| `propertyID` | object |  |
| `sentDate` | string |  |
| `startDate` | object |  |
| `status` | object |  |
| `subject` | string |  |
| `workTicketID` | object |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Activities` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

