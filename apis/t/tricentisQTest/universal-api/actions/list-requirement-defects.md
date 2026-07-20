# Tricentis qTest: List Requirement Defects

Retrieves requirement defects from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-requirement-defects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-requirement-defects?connectionId=$CONNECTION_ID&projectId=1&requirementId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "requirementId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-requirement-defects?${params}`, {
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
| `requirementId` | number | yes | ID of the Requirement. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connection_id": 1,
      "external_defect_id": "string",
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
| `id` | number |  |
| `name` | string |  |
| `web_url` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/requirements/{requirementId}/defects` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-requirement-defects.md) for the provider-specific parameters and requirements.

