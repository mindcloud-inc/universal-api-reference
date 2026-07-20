# NetHunt CRM: Find Recently Updated Records

Finds recently updated records in NetHunt CRM.

```
GET https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-updated-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-updated-records?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-updated-records?${params}`, {
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
| `fieldName` | string | no | Optional field name to limit updates observed. Can be provided more than once. |
| `folderId` | string | yes | Folder ID to watch for updated records. |
| `since` | string | no | Only records updated after this ISO timestamp are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "link": "https://example.com",
      "recordId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fields` | object |  |
| `id` | string |  |
| `link` | string |  |
| `recordId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `GET /triggers/updated-record/:folderId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-recently-updated-records.md) for the provider-specific parameters and requirements.

