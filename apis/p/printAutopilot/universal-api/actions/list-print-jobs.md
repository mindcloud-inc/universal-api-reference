# Print Autopilot: List Print Jobs

Retrieves print jobs from Print Autopilot.

```
GET https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print Autopilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "base64": "string",
          "file_name": "Ava Chen",
          "id": 1,
          "printable_queue_id": 1
        }
      ],
      "PaperSize": {
        "height": 1,
        "id": 1,
        "name": "Ava Chen",
        "rawKind": "string",
        "width": 1
      },
      "Printer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "scaling": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents[].base64` | string |  |
| `documents[].file_name` | string |  |
| `documents[].id` | number |  |
| `documents[].printable_queue_id` | number |  |
| `PaperSize.height` | number |  |
| `PaperSize.id` | number |  |
| `PaperSize.name` | string |  |
| `PaperSize.rawKind` | string |  |
| `PaperSize.width` | number |  |
| `Printer.id` | number |  |
| `Printer.name` | string |  |
| `scaling` | number |  |

## Native endpoint

Through the native Print Autopilot API, this operation is `GET /print-jobs` (base URL `https://printautopilot.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-print-jobs.md) for the provider-specific parameters and requirements.

