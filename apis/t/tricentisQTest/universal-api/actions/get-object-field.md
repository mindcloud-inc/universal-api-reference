# Tricentis qTest: Get Object Field

Retrieves an object field from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-object-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-object-field?connectionId=$CONNECTION_ID&projectId=1&objectType=string&fieldId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "objectType": "string",
  "fieldId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-object-field?${params}`, {
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
| `objectType` | string | yes | Object type, such as releases, builds, requirements, test-cases, test-steps, defects, or test-runs. |
| `fieldId` | number | yes | ID of the custom field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowed_values": [
        {}
      ],
      "attribute_type": "string",
      "constrained": true,
      "id": 1,
      "label": "string",
      "multiple": true,
      "required": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed_values` | array<object> |  |
| `attribute_type` | string |  |
| `constrained` | boolean |  |
| `id` | number |  |
| `label` | string |  |
| `multiple` | boolean |  |
| `required` | boolean |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/settings/{objectType}/fields/{fieldId}` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object-field.md) for the provider-specific parameters and requirements.

