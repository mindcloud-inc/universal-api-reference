# Codemagic: Start App Preview

Creates a new app preview for a Codemagic build.

```
POST https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/start-app-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/start-app-preview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buildId": "string",
  "artifactPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/start-app-preview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buildId": "string",
    "artifactPath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buildId` | string | yes | Codemagic build identifier. |
| `artifactPath` | string | yes | Path of the build artifact to preview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | date |  |
| `id` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `POST /api/v3/builds/:build_id/preview` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-app-preview.md) for the provider-specific parameters and requirements.

