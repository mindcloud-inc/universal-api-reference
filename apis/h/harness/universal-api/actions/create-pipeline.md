# Harness: Create Pipeline

Creates a new pipeline in Harness.

```
POST https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-pipeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Pipeline description. |
| `identifier` | string | yes | Pipeline identifier. |
| `name` | string | yes | Pipeline display name. |

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
| `data` | object | Created pipeline payload. |
| `metaData` | object | Optional Harness metadata. |
| `status` | string | Harness API status. |

## Native endpoint

Through the native Harness API, this operation is `POST https://app.harness.io/pipeline/api/pipelines/v2?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pipeline.md) for the provider-specific parameters and requirements.

