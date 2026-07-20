# NetHunt CRM: Find Recent Record Changes

Finds recent record changes in NetHunt CRM.

```
GET https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recent-record-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recent-record-changes?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recent-record-changes?${params}`, {
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
| `fieldName` | string | no | Optional field name to limit changes observed. Can be provided more than once. |
| `folderId` | string | yes | Folder ID to inspect for record changes. |
| `recordId` | string | no | Optional record ID to limit the result to a single record. |
| `since` | string | no | Only changes made after this ISO timestamp are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldActions": {},
      "id": "string",
      "recordAction": "string",
      "recordId": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldActions` | object |  |
| `id` | string |  |
| `recordAction` | string |  |
| `recordId` | string |  |
| `time` | date |  |
| `user` | object |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `GET /triggers/record-change/:folderId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-recent-record-changes.md) for the provider-specific parameters and requirements.

