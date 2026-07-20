# Less Annoying CRM: List Notes



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/list-notes?${params}`, {
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
| `sortDirection` | string | no | Ascending or Descending note order by date. |
| `dateFilterStart` | date | no | Only return notes on or after this date/time. |
| `dateFilterEnd` | date | no | Only return notes on or before this date/time. |
| `userFilter` | string | no | JSON array of UserIds to filter by author. |
| `contactId` | string | no | Only return notes attached to this contact. |
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDisplayedInHistory": "2026-05-07T12:00:00.000Z",
      "isRichText": true,
      "note": "string",
      "noteId": "string",
      "pipelineInfo": {
        "pipelineId": "string",
        "pipelineItemId": "string",
        "pipelineMetaData": {
          "name": "Ava Chen"
        },
        "previousStatusId": "string",
        "statusId": "string",
        "statusMetaData": {
          "name": "Ava Chen"
        }
      },
      "userId": "string",
      "userMetaData": {
        "firstName": "Ava",
        "lastName": "Chen"
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
| `dateCreated` | date |  |
| `dateDisplayedInHistory` | date |  |
| `isRichText` | boolean |  |
| `note` | string |  |
| `noteId` | string |  |
| `pipelineInfo.pipelineId` | string |  |
| `pipelineInfo.pipelineItemId` | string |  |
| `pipelineInfo.pipelineMetaData.name` | string |  |
| `pipelineInfo.previousStatusId` | string |  |
| `pipelineInfo.statusId` | string |  |
| `pipelineInfo.statusMetaData.name` | string |  |
| `userId` | string |  |
| `userMetaData.firstName` | string |  |
| `userMetaData.lastName` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

