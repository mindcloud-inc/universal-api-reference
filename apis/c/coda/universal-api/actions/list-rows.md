# Coda: List Rows

Retrieves rows from a Coda table.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&docId=string&tableIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "docId": "string",
  "tableIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-rows?${params}`, {
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
| `docId` | list | yes |  |
| `tableIdOrName` | list | yes |  |
| `query` | string | no |  |
| `useColumnNames` | boolean | no |  |
| `valueFormat` | string | no |  |
| `visibleOnly` | boolean | no |  |
| `syncToken` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": "string",
      "index": 1,
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "values": {
        "c55IWR0eDV": "string",
        "cBdDPeDrw2T": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browserLink` | string |  |
| `createdAt` | date |  |
| `href` | string |  |
| `id` | string |  |
| `index` | number |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `values.c55IWR0eDV` | string |  |
| `values.cBdDPeDrw2T` | date |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables/:tableIdOrName/rows` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rows.md) for the provider-specific parameters and requirements.

