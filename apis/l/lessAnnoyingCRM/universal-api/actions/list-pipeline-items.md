# Less Annoying CRM: List Pipeline Items



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-items?connectionId=$CONNECTION_ID&pipelineId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-pipeline-items?${params}`, {
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
| `pipelineId` | string | yes | The pipeline Id to search within. |
| `userFilter` | string | no | JSON array of UserIds to filter by related contact owner. |
| `statusFilter` | string | no | JSON array of StatusIds to restrict the result set. |
| `advancedFilters` | string | no | JSON array of advanced pipeline filter objects. |
| `sortBy` | string | no | Field used for sorting. |
| `sortDirection` | string | no | Ascending or Descending sort order. |
| `maxNumberOfResults` | number | no | Maximum number of results to return. |
| `page` | number | no | Pagination page number starting at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "contactMetaData": {
        "assignedTo": "string",
        "name": "Ava Chen"
      },
      "createdBy": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "lastNote": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "lastUpdatedBy": "string",
      "numberOfUpdates": 1,
      "pipelineId": "string",
      "pipelineItemId": "string",
      "pipelineMetaData": {
        "name": "Ava Chen"
      },
      "statusId": "string",
      "statusMetaData": {
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `contactMetaData.assignedTo` | string |  |
| `contactMetaData.name` | string |  |
| `createdBy` | string |  |
| `dateCreated` | date |  |
| `lastNote` | string |  |
| `lastUpdate` | date |  |
| `lastUpdatedBy` | string |  |
| `numberOfUpdates` | number |  |
| `pipelineId` | string |  |
| `pipelineItemId` | string |  |
| `pipelineMetaData.name` | string |  |
| `statusId` | string |  |
| `statusMetaData.name` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipeline-items.md) for the provider-specific parameters and requirements.

