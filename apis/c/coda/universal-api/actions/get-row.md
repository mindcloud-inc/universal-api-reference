# Coda: Get Row

Retrieves row details from a Coda table.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-row?connectionId=$CONNECTION_ID&docId=string&tableIdOrName=Ava%20Chen&rowIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableIdOrName": "Ava Chen",
  "rowIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/get-row?${params}`, {
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
| `rowIdOrName` | list | yes |  |
| `useColumnNames` | boolean | no |  |
| `valueFormat` | string | no |  |

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
      "parent": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "name": "Ava Chen",
        "tableType": "string",
        "type": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "values": {
        "c55Iwr0eDv": "string",
        "cBdDpeDrw2T": "2026-05-07T12:00:00.000Z"
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
| `parent.browserLink` | string |  |
| `parent.href` | string |  |
| `parent.id` | string |  |
| `parent.name` | string |  |
| `parent.tableType` | string |  |
| `parent.type` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `values.c55Iwr0eDv` | string |  |
| `values.cBdDpeDrw2T` | date |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row.md) for the provider-specific parameters and requirements.

