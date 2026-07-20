# Coda: Delete Row

Deletes a row from a Coda table.

```
DELETE https://connect.mindcloud.co/v1/universal/coda/latest/actions/delete-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/coda/latest/actions/delete-row?connectionId=$CONNECTION_ID&docId=string&tableIdOrName=Ava%20Chen&rowIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "tableIdOrName": "Ava Chen",
  "rowIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/delete-row?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `requestId` | string |  |

## Native endpoint

Through the native Coda API, this operation is `DELETE /docs/:docId/tables/:tableIdOrName/rows/:rowIdOrName` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-row.md) for the provider-specific parameters and requirements.

