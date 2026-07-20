# OnePageCRM: List Notes

Retrieves notes from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-notes?${params}`, {
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
| `contactId` | string | no | Return notes for a specific contact. Example: `5ae06ef9d55673108fe8877b`. |
| `companyId` | string | no | Return notes for a specific company. Example: `6se06df9d55673108re84745`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFilter` | list<string> | no | Choose which date field to use with Since or Until. One of: `created_at`, `date`, `modified_at`, `updated_at`. |
| `since` | date | no | Return notes added or edited since this date or timestamp. Example: `2018-07-01`. |
| `until` | date | no | Return notes added or edited until this date or timestamp. Example: `2018-07-31`. |
| `modifiedSince` | date | no | Return only notes modified since this date or timestamp. Example: `2018-07-01`. |
| `unmodifiedSince` | date | no | Return only notes unmodified since this date or timestamp. Example: `2018-07-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "maxPage": 1,
      "notes": [
        {
          "note": {
            "author": "string",
            "contactId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "date": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
            "linkedDealId": "https://example.com",
            "linkedDealName": "https://example.com",
            "modifiedAt": "2026-05-07T12:00:00.000Z",
            "text": "string"
          }
        }
      ],
      "page": 1,
      "perPage": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maxPage` | number |  |
| `notes[].note.author` | string |  |
| `notes[].note.contactId` | string |  |
| `notes[].note.createdAt` | date |  |
| `notes[].note.date` | date |  |
| `notes[].note.id` | string |  |
| `notes[].note.lastTimelineUpdate` | date |  |
| `notes[].note.linkedDealId` | string |  |
| `notes[].note.linkedDealName` | string |  |
| `notes[].note.modifiedAt` | date |  |
| `notes[].note.text` | string |  |
| `page` | number |  |
| `perPage` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /notes` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

