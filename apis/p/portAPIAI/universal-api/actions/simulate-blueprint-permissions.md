# Port API AI: Simulate Blueprint Permissions

Retrieves simulated blueprint permissions from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/simulate-blueprint-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/simulate-blueprint-permissions?connectionId=$CONNECTION_ID&blueprintIdentifier=string&operation=string&userIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintIdentifier": "string",
  "operation": "string",
  "userIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/simulate-blueprint-permissions?${params}`, {
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
| `blueprintIdentifier` | string | yes | The blueprint identifier. |
| `operation` | string | yes | The operation to simulate. |
| `userIdentifier` | string | yes | The user identifier to simulate permissions for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints/:blueprint_identifier/permissions/simulate` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/simulate-blueprint-permissions.md) for the provider-specific parameters and requirements.

