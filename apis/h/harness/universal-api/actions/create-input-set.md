# Harness: Create Input Set

Creates a new input set in Harness.

```
POST https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-input-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-input-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "message": "string",
  "name": "Ava Chen",
  "pipelineIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-input-set', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "message": "string",
    "name": "Ava Chen",
    "pipelineIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Input set identifier. |
| `message` | string | yes | Approval message runtime value. |
| `name` | string | yes | Input set display name. |
| `pipelineIdentifier` | string | yes | Pipeline identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "correlationId": "string",
      "data": {},
      "metaData": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `correlationId` | string | Harness correlation identifier. |
| `data` | object | Created input set payload. |
| `metaData` | object | Optional Harness metadata. |
| `status` | string | Harness API status. |

## Native endpoint

Through the native Harness API, this operation is `POST https://app.harness.io/pipeline/api/inputSets?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier&pipelineIdentifier=:pipelineIdentifier` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-input-set.md) for the provider-specific parameters and requirements.

