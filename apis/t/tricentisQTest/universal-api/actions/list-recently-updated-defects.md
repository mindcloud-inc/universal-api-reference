# Tricentis qTest: List Recently Updated Defects

Retrieves recently updated defects from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-recently-updated-defects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-recently-updated-defects?connectionId=$CONNECTION_ID&projectId=1&startTime=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "startTime": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-recently-updated-defects?${params}`, {
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
| `startTime` | string | yes | URL-encoded timestamp since when defects have been updated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connection_id": 1,
      "external_defect_id": "string",
      "external_project_id": "string",
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
| `connection_id` | number |  |
| `external_defect_id` | string |  |
| `external_project_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `web_url` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/defects/last-change` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recently-updated-defects.md) for the provider-specific parameters and requirements.

