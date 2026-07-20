# Optimizely: Get Project

Retrieves project details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=4844790198566912" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "4844790198566912"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | The Optimizely project id. Default: `4844790198566912`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "confidenceThreshold": 1,
      "created": "string",
      "id": 1,
      "isClassic": true,
      "isFlagsEnabled": true,
      "lastModified": "string",
      "name": "Ava Chen",
      "platform": "string",
      "status": "string",
      "webSnippet": {
        "codeRevision": 1,
        "library": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `confidenceThreshold` | number |  |
| `created` | string |  |
| `id` | number |  |
| `isClassic` | boolean |  |
| `isFlagsEnabled` | boolean |  |
| `lastModified` | string |  |
| `name` | string |  |
| `platform` | string |  |
| `status` | string |  |
| `webSnippet.codeRevision` | number |  |
| `webSnippet.library` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /projects/{projectId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

