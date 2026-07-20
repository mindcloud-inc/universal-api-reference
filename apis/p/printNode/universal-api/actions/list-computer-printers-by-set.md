# PrintNode: List Computer Printers by Set

Retrieves specific printers for specific computers from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computer-printers-by-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computer-printers-by-set?connectionId=$CONNECTION_ID&computerSet=string&printerSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "computerSet": "string",
  "printerSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-computer-printers-by-set?${params}`, {
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
| `computerSet` | string | yes | Comma-separated PrintNode computer IDs. |
| `printerSet` | string | yes | Comma-separated PrintNode printer IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {},
      "computer": {
        "createTimestamp": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "state": "string"
      },
      "createTimestamp": "2026-05-07T12:00:00.000Z",
      "default": true,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | object | Printer capability summary reported by PrintNode. |
| `computer.createTimestamp` | date | Timestamp when the owning computer was first registered. |
| `computer.id` | number | Owning computer identifier. |
| `computer.name` | string | Owning computer name. |
| `computer.state` | string | Owning computer connection state. |
| `createTimestamp` | date | Timestamp when the printer was first reported. |
| `default` | boolean | Whether the printer is the default printer. |
| `description` | string | Printer description. |
| `id` | number | Printer identifier. |
| `name` | string | Printer name. |
| `state` | string | Printer state. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /computers/:computerSet/printers/:printerSet` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-computer-printers-by-set.md) for the provider-specific parameters and requirements.

