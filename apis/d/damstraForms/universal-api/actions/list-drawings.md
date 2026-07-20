# Damstra Forms: List Drawings

Retrieves drawings from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-drawings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-drawings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-drawings?${params}`, {
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
| `projectId` | number | no | Only return results belonging to the project with the specified id. Default: `null (All projects)`. Example: `1`. |
| `updatedFrom` | string | no | Only return results updated after the specified value. It will try to make sense of whatever datetime format you provide, but the example shows the officially supported format. Example: `2016-12-31T13:50:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "current": true,
      "discipline": "string",
      "docType": "string",
      "href": "string",
      "id": 1,
      "name": "Ava Chen",
      "number": "string",
      "projectId": 1,
      "revision": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "wbsItemId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | From Damstra Forms API example response. |
| `current` | boolean | From Damstra Forms API example response. |
| `discipline` | string | From Damstra Forms API example response. |
| `docType` | string | From Damstra Forms API example response. |
| `href` | string | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `number` | string | From Damstra Forms API example response. |
| `projectId` | number | From Damstra Forms API example response. |
| `revision` | string | From Damstra Forms API example response. |
| `status` | string | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `wbsItemId` | number | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /drawings` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-drawings.md) for the provider-specific parameters and requirements.

