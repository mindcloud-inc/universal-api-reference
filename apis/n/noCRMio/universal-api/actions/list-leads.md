# noCRM.io: List Leads

Retrieves leads from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads?${params}`, {
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
| `dateRangeType` | string | no | Which lead date to use for the date range. |
| `email` | string | no | Filter leads that contain an email address. |
| `endDate` | string | no | End of the date range filter. |
| `fieldKey` | string | no | Custom-field key used together with Field Value. |
| `fieldValue` | string | no | Value for the selected custom-field key. |
| `includeUnassigned` | string | no | Include unassigned leads in the results. |
| `starred` | string | no | Return only starred leads when true. |
| `startDate` | string | no | Start of the date range filter. |
| `status` | string | no | Filter leads by one or more statuses. |
| `step` | string | no | Filter leads by step names or step IDs. |
| `tags` | string | no | Return leads that contain all specified tags. |
| `updatedAfter` | string | no | Return leads updated after this date. |
| `userId` | string | no | Filter leads assigned to a specific user ID or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "clientFolderId": 1,
      "clientFolderName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "pipeline": "string",
      "probability": 1,
      "starred": true,
      "status": "string",
      "step": "string",
      "stepId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `clientFolderId` | number |  |
| `clientFolderName` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `pipeline` | string |  |
| `probability` | number |  |
| `starred` | boolean |  |
| `status` | string |  |
| `step` | string |  |
| `stepId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /leads` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

