# PrintNode: Cancel Printer Print Jobs by Set

Cancels specific undelivered print jobs for specific printers in PrintNode.

```
DELETE https://connect.mindcloud.co/v1/universal/printNode/latest/actions/cancel-printer-print-jobs-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/cancel-printer-print-jobs-by-set?connectionId=$CONNECTION_ID&printerSet=string&printJobSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "printerSet": "string",
  "printJobSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/cancel-printer-print-jobs-by-set?${params}`, {
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
      "value": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<number> | IDs of the print jobs cancelled by the delete request. |

## Native endpoint

Through the native PrintNode API, this operation is `DELETE /printers/:printerSet/printjobs/:printJobSet` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-printer-print-jobs-by-set.md) for the provider-specific parameters and requirements.

