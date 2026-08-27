# Acumatica: List Projects



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&wse=string&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "wse": "string",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-projects?${params}`, {
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
| `wse` | string | yes |  |
| `version` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand` | string | no | Use the $expand parameter to specify the linked and detail entities that should be expanded. By default, no linked or detail entities are expanded; that is, only fields of the top-level entity are returned. You need to explicitly specify each linked or detail entity to be expanded. |
| `select` | string | no | When you retrieve records from Acumatica ERP by using the contract-based REST API, you use the $select parameter to specify the fields of the entity to be returned from Acumatica ERP. By default, all fields of the entity are returned. |
| `filter` | string | no |  |

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
          "note": {},
          "refNoteID": {
            "value": "string"
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
| `attributes[].note` | object |  |
| `attributes[].refNoteID.value` | string |  |
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

Through the native Acumatica API, this operation is `GET /entity/:wse/:version/Project` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

