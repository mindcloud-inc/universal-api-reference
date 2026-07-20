# Planning Center: List Person Field Data

Retrieves field data for a person in Planning Center.

```
GET https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-field-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planning Center `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-field-data?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-person-field-data?${params}`, {
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
| `personId` | string | yes | The person id. |
| `include` | string | no | Include associated field_definition, field_option, or tab records in the response. |
| `order` | string | no | Sort field data by a supported field; prefix the field with a hyphen for descending order. |
| `where` | object | no | Field-qualified field data query filters. |
| `where.fieldDefinitionId` | number | no | Query field data by an exact related field_definition id. |
| `where.file` | string | no | Query field data by an exact file value. |
| `where.fileContentType` | string | no | Query field data by an exact file_content_type value. |
| `where.fileName` | string | no | Query field data by an exact file_name value. |
| `where.fileSize` | number | no | Query field data by an exact file_size value. |
| `where.value` | string | no | Query field data by an exact value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "file": "string",
        "fileContentType": "string",
        "fileName": "Ava Chen",
        "fileSize": 1,
        "value": "string"
      },
      "id": "string",
      "relationships": {
        "customizable": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "fieldDefinition": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.file` | string |  |
| `attributes.fileContentType` | string |  |
| `attributes.fileName` | string |  |
| `attributes.fileSize` | number |  |
| `attributes.value` | string |  |
| `id` | string |  |
| `relationships.customizable.data.id` | string |  |
| `relationships.customizable.data.type` | string |  |
| `relationships.fieldDefinition.data.id` | string |  |
| `relationships.fieldDefinition.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Planning Center API, this operation is `GET /people/v2/people/:person_id/field_data` (base URL `https://api.planningcenteronline.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-person-field-data.md) for the provider-specific parameters and requirements.

