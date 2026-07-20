# Survalyzer: List Artifacts



```
GET https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-artifacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-artifacts?${params}`, {
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
| `path` | string | no | Artifact folder path to list, for example Images. |
| `workspaceId` | number | no | Workspace identifier to search for artifacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artifacts": [
        {}
      ],
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artifacts` | array<object> |  |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Common/v3/ReadArtifactList` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-artifacts.md) for the provider-specific parameters and requirements.

