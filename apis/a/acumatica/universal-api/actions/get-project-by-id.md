# Acumatica: Get Project by ID



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-by-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-project-by-id?${params}`, {
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
| `select` | string | no | Default: `Attributes `. |
| `expand` | string | no |  |
| `projectId` | string | yes | The ID of a project to retrieve. Provided when you list Projects. Use the links.self property. Example: /entity/Default/23.200.001/Project/e7d81cfc-f596-ef11-8361-0646c1159ab3 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": {
        "value": 1
      },
      "attributes": [
        {
          "attributeDescription": {
            "value": "string"
          },
          "attributeID": {
            "value": "string"
          },
          "id": "string",
          "Links": {
            "files:put": "https://example.com"
          },
          "note": {},
          "refNoteID": {
            "value": "string"
          },
          "required": {
            "value": true
          },
          "rowNumber": 1,
          "value": {
            "value": "string"
          },
          "valueDescription": {
            "value": "string"
          }
        }
      ],
      "customer": {
        "value": "string"
      },
      "description": {
        "value": "string"
      },
      "expenses": {
        "value": 1
      },
      "hold": {
        "value": true
      },
      "id": "string",
      "income": {
        "value": 1
      },
      "lastModifiedDateTime": {
        "value": "string"
      },
      "liabilities": {
        "value": 1
      },
      "Links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "note": {
        "value": "string"
      },
      "projectID": {
        "value": "string"
      },
      "projectTemplateID": {
        "value": "string"
      },
      "rowNumber": 1,
      "status": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets.value` | number |  |
| `attributes[].attributeDescription.value` | string |  |
| `attributes[].attributeID.value` | string |  |
| `attributes[].id` | string |  |
| `attributes[].Links.files:put` | string |  |
| `attributes[].note` | object |  |
| `attributes[].refNoteID.value` | string |  |
| `attributes[].required.value` | boolean |  |
| `attributes[].rowNumber` | number |  |
| `attributes[].value.value` | string |  |
| `attributes[].valueDescription.value` | string |  |
| `customer.value` | string |  |
| `description.value` | string |  |
| `expenses.value` | number |  |
| `hold.value` | boolean |  |
| `id` | string |  |
| `income.value` | number |  |
| `lastModifiedDateTime.value` | string |  |
| `liabilities.value` | number |  |
| `Links.files:put` | string |  |
| `Links.self` | string |  |
| `note.value` | string |  |
| `projectID.value` | string |  |
| `projectTemplateID.value` | string |  |
| `rowNumber` | number |  |
| `status.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /:projectId` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-id.md) for the provider-specific parameters and requirements.

