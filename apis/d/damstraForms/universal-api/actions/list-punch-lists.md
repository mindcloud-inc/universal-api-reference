# Damstra Forms: List Punch Lists

Retrieves punch lists from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-punch-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-punch-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-punch-lists?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Only return forms associate with the specified project. Example: `101`. |
| `status` | string | no | Statuses to include in returned results. You can combine statuses by separating them with "\|" (e.g. draft\|open, open\|closed, etc.) One of: `0`, `1`, `2`. Accepts multiple values in one string, delimited by `\|`. Default: `draft\|open\|closed`. Example: `closed`. |
| `updatedFrom` | string | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. Example: `2016-12-31T13:50:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientCreatedAt": "2026-05-07T12:00:00.000Z",
      "clientUpdatedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "draftTemplateId": 1,
      "id": 1,
      "name": "Ava Chen",
      "ownedByUserId": 1,
      "projectId": 1,
      "status": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientCreatedAt` | date | From Damstra Forms API example response. |
| `clientUpdatedAt` | date | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `createdByUserId` | number | From Damstra Forms API example response. |
| `draftTemplateId` | number | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `ownedByUserId` | number | From Damstra Forms API example response. |
| `projectId` | number | From Damstra Forms API example response. |
| `status` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /punch_lists` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-punch-lists.md) for the provider-specific parameters and requirements.

