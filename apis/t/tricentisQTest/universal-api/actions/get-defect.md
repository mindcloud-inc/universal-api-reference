# Tricentis qTest: Get Defect

Retrieves a defect from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect?connectionId=$CONNECTION_ID&projectId=1&defectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "defectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect?${params}`, {
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
| `defectId` | string | yes | ID of the defect. |

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
| `web_url` | string |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/defects/{defectId}` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-defect.md) for the provider-specific parameters and requirements.

