# Microsoft Power BI: Create Workspace



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud MC-21089 Verification"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud MC-21089 Verification"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the new Power BI workspace. Example: `MindCloud MC-21089 Verification`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isOnDedicatedCapacity": true,
      "isReadOnly": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The workspace ID. |
| `isOnDedicatedCapacity` | boolean | Whether the workspace is assigned to dedicated capacity. |
| `isReadOnly` | boolean | Whether the workspace is read-only. |
| `name` | string | The workspace name. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

