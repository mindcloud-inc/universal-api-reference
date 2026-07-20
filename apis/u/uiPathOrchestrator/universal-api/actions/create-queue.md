# UiPath Orchestrator: Create queue



```
POST https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-queue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UiPath Orchestrator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/create-queue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Queue name. |
| `description` | string | no | Queue description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "EnforceUniqueReference": true,
      "Id": 1,
      "MaxNumberOfRetries": 1,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string |  |
| `EnforceUniqueReference` | boolean |  |
| `Id` | number |  |
| `MaxNumberOfRetries` | number |  |
| `Name` | string |  |

## Native endpoint

Through the native UiPath Orchestrator API, this operation is `POST /odata/QueueDefinitions` (base URL `https://cloud.uipath.com/{{credentials.organizationName}}/{{credentials.tenantName}}/orchestrator_`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-queue.md) for the provider-specific parameters and requirements.

