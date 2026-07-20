# DecisionVault: Create Matter

Creates a matter in DecisionVault and returns an invite link.

```
POST https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/create-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/create-matter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "matterName": "Ava Chen",
  "questionnaireId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/create-matter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "matterName": "Ava Chen",
    "questionnaireId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | object | no | Optional context object with up to five string or integer key-value pairs. |
| `matterName` | string | yes | The matter name to create in DecisionVault. |
| `questionnaireId` | string | yes | The questionnaire ID to use when pre-creating the matter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "invite_key": "string",
      "invite_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `invite_key` | string |  |
| `invite_url` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `POST /matters/create` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-matter.md) for the provider-specific parameters and requirements.

