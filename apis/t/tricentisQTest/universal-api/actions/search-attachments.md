# Tricentis qTest: Search Attachments

Finds attachments in Tricentis qTest by object criteria.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/search-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/search-attachments?connectionId=$CONNECTION_ID&projectId=1&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/search-attachments?${params}`, {
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
| `type` | string | yes | Artifact type to search attachments for, such as releases, builds, requirements, test-cases, test-logs, test-steps, or defects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "content_type": "string",
      "created_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "web_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `content_type` | string |  |
| `created_date` | date |  |
| `id` | number |  |
| `name` | string |  |
| `web_url` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/attachments` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-attachments.md) for the provider-specific parameters and requirements.

