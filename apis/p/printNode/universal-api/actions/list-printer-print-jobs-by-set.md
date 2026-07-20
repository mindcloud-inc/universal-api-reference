# PrintNode: List Printer Print Jobs by Set

Retrieves specific print jobs for specific printers from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-printer-print-jobs-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-printer-print-jobs-by-set?connectionId=$CONNECTION_ID&printerSet=string&printJobSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "printerSet": "string",
  "printJobSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-printer-print-jobs-by-set?${params}`, {
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
| `printerSet` | string | yes | Comma-separated PrintNode printer IDs. |
| `printJobSet` | string | yes | Comma-separated PrintNode print job IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createTimestamp": "2026-05-07T12:00:00.000Z",
      "expireAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "printer": {
        "description": "string",
        "id": 1,
        "name": "Ava Chen",
        "state": "string"
      },
      "source": "string",
      "state": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Type of content submitted to PrintNode. |
| `createTimestamp` | date | Timestamp when the print job was created. |
| `expireAt` | date | Expiration timestamp for the print job when present. |
| `id` | number | Print job identifier. |
| `printer.description` | string | Printer description for the print job. |
| `printer.id` | number | Printer identifier for the print job. |
| `printer.name` | string | Printer name for the print job. |
| `printer.state` | string | Printer state for the print job. |
| `source` | string | Source description for the print job. |
| `state` | string | Current print job state. |
| `title` | string | Print job title. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /printers/:printerSet/printjobs/:printJobSet` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-printer-print-jobs-by-set.md) for the provider-specific parameters and requirements.

