# UiPath Orchestrator: Get robot



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-robot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-robot?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-robot?${params}`, {
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
| `id` | number | yes | The numeric robot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "MachineName": "Ava Chen",
      "Name": "Ava Chen",
      "Type": "string",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |
| `MachineName` | string |  |
| `Name` | string |  |
| `Type` | string |  |
| `Username` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Robots(:id)` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-robot.md) for the provider-specific parameters and requirements.

