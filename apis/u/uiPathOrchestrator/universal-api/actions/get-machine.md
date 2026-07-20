# UiPath Orchestrator: Get machine



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-machine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-machine?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-machine?${params}`, {
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
| `id` | number | yes | The numeric machine ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "LicenseKey": "string",
      "Name": "Ava Chen",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |
| `LicenseKey` | string |  |
| `Name` | string |  |
| `Type` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Machines(:id)` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-machine.md) for the provider-specific parameters and requirements.

