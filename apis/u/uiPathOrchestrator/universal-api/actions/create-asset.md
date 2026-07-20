# UiPath Orchestrator: Create asset



```
POST https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "valueScope": "Global",
  "valueType": "Text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "valueScope": "Global",
    "valueType": "Text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Asset name. |
| `valueScope` | string | yes | Asset scope, usually Global. Default: `Global`. |
| `valueType` | string | yes | Asset value type, such as Text, Bool, Integer, or Credential. Default: `Text`. |
| `stringValue` | string | no | Text value for Text assets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "Name": "Ava Chen",
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
| `Id` | number |  |
| `Name` | string |  |
| `Value` | string |  |
| `ValueScope` | string |  |
| `ValueType` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `POST /odata/Assets` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset.md) for the provider-specific parameters and requirements.

