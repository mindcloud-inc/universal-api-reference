# Tricentis qTest: List Linked Artifacts

Retrieves linked artifacts from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-linked-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-linked-artifacts?connectionId=$CONNECTION_ID&projectId=1&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-linked-artifacts?${params}`, {
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
| `projectId` | number | yes | ID of the qTest project. |
| `type` | string | yes | Artifact type such as releases, builds, requirements, test-cases, test-runs, test-logs, test-steps, or defects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "link_type": "https://example.com",
      "objects": [
        {}
      ],
      "pid": "string",
      "self": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `link_type` | string |  |
| `objects` | array<object> |  |
| `pid` | string |  |
| `self` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/linked-artifacts` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linked-artifacts.md) for the provider-specific parameters and requirements.

