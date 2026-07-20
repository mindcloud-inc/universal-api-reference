# Buildkite: Create Annotation

Creates a build annotation in Buildkite.

```
POST https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buildkite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "build": "string",
  "organization": "string",
  "pipeline": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/create-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "build": "string",
    "organization": "string",
    "pipeline": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | The markdown body of the annotation. |
| `build` | string | yes | The Buildkite build number or UUID, depending on the endpoint. |
| `context` | string | no | The annotation context label. |
| `organization` | string | yes | The Buildkite organization slug. |
| `pipeline` | string | yes | The Buildkite pipeline slug. |
| `style` | string | no | The annotation style, such as success, info, warning, or error. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "context": "string",
      "createdAt": "string",
      "id": "string",
      "style": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `context` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `style` | string |  |

## Native endpoint

Through the native Buildkite API, this operation is `POST /organizations/:organization/pipelines/:pipeline/builds/:build/annotations` (base URL `https://api.buildkite.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-annotation.md) for the provider-specific parameters and requirements.

