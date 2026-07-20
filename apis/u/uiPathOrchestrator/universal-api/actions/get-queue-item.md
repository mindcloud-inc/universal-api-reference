# UiPath Orchestrator: Get queue item



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-queue-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-queue-item?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-queue-item?${params}`, {
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
| `id` | number | yes | The numeric queue item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "Key": "string",
      "Priority": "string",
      "Reference": "string",
      "SpecificContent": {},
      "Status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |
| `Key` | string |  |
| `Priority` | string |  |
| `Reference` | string |  |
| `SpecificContent` | object |  |
| `Status` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/QueueItems(:id)` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue-item.md) for the provider-specific parameters and requirements.

