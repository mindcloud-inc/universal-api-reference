# Zoho CRM: Get Notes for Record

Retrieves notes for a Zoho CRM record.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-notes-for-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-notes-for-record?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleApiName=Leads&recordId=7323083000000731821&fields=Owner%2CParent_Id%2CNote_Title%2CNote_Content%2CCreated_Time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleApiName": "Leads",
  "recordId": "7323083000000731821",
  "fields": "Owner,Parent_Id,Note_Title,Note_Content,Created_Time"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-notes-for-record?${params}`, {
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
| `moduleApiName` | string | yes | Parent module API name. Example: `Leads`. |
| `recordId` | string | yes | Parent record ID. Example: `7323083000000731821`. |
| `fields` | string | yes | Comma-separated note fields to return. Example: `Owner,Parent_Id,Note_Title,Note_Content,Created_Time`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "noteContent": "string",
      "noteTitle": "string",
      "parentId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Note creation timestamp. |
| `id` | string | Note ID. |
| `noteContent` | string | Note content. |
| `noteTitle` | string | Note title. |
| `parentId` | object | Parent record reference. |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /:module_api_name/:record_id/Notes` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-notes-for-record.md) for the provider-specific parameters and requirements.

