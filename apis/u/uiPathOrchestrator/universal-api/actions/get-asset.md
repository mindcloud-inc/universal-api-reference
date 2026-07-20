# UiPath Orchestrator: Get asset



```
GET https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/get-asset?${params}`, {
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
| `id` | number | yes | The numeric asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BoolValue": true,
      "Id": 1,
      "IntValue": 1,
      "Name": "Ava Chen",
      "StringValue": "string",
      "Value": "string",
      "ValueScope": "string",
      "ValueType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BoolValue` | boolean |  |
| `Id` | number |  |
| `IntValue` | number |  |
| `Name` | string |  |
| `StringValue` | string |  |
| `Value` | string |  |
| `ValueScope` | string |  |
| `ValueType` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `GET /odata/Assets(:id)` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

