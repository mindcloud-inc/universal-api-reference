# Acumatica: Get Entity Schema

Get a specific Entity schema from the 'Default' Acumatica Endpoint.

```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/entity-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/entity-schema?connectionId=$CONNECTION_ID&entity=ProFormaInvoice&endpointVersion=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity": "ProFormaInvoice",
  "endpointVersion": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/entity-schema?${params}`, {
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
| `entity` | list<string> | yes | The top-level entity to retrieve. Example: "Project" or "User" One of: `ProFormaInvoice`, `Project`, `ProjectBudget`, `ProjectTask`, `SalesOrder`. |
| `endpointVersion` | list<string> | yes |  |

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

Through the native Acumatica API, this operation is `GET /entity/Default/:endpointVersion/:entity/$adHocSchema` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/entity-schema.md) for the provider-specific parameters and requirements.

