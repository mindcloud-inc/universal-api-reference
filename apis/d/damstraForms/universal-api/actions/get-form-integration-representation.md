# Damstra Forms: Get Form Integration Representation

Retrieves a form in integration format from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-form-integration-representation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-form-integration-representation?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-form-integration-representation?${params}`, {
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
| `id` | number | yes | The unique identifier of the form. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `representation` | string | no | If "integration" is specified will display the form using integration tags Example: `integration`. |
| `includeChildren` | boolean | no | If true the metadata section will include information about any linked child forms or actions Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": {
        "customTag": {
          "properties": {
            "property1": "string",
            "property2": "string"
          },
          "value": "string"
        }
      },
      "fields": {
        "customTag": {
          "linked": {
            "href": "https://example.com",
            "id": 1,
            "signedHref": "https://example.com",
            "type": "https://example.com",
            "uuid": "https://example.com"
          },
          "properties": {
            "property1": "string",
            "property2": "string"
          },
          "signature": {
            "contentType": "string",
            "href": "string",
            "id": 1,
            "signedHref": "string",
            "userId": 1
          },
          "value": "string"
        }
      },
      "metadata": {
        "children": {
          "href": "string",
          "id": 1,
          "pdfHref": "string",
          "uuid": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "creator": {
          "href": "string",
          "id": 1,
          "uuid": "string"
        },
        "href": "string",
        "id": 1,
        "owner": {
          "id": 1,
          "uuid": "string"
        },
        "project": {
          "id": 1,
          "uuid": "string"
        },
        "status": 1,
        "template": {
          "draftTemplate": {
            "href": "string",
            "id": 1
          },
          "href": "string",
          "id": 1
        },
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> | From Damstra Forms API example response. |
| `columns.customTag` | array<object> | From Damstra Forms API example response. |
| `columns.customTag.properties` | object | From Damstra Forms API example response. |
| `columns.customTag.properties.property1` | string | From Damstra Forms API example response. |
| `columns.customTag.properties.property2` | string | From Damstra Forms API example response. |
| `columns.customTag.value` | string | From Damstra Forms API example response. |
| `fields` | array<object> | From Damstra Forms API example response. |
| `fields.customTag` | object | From Damstra Forms API example response. |
| `fields.customTag.linked` | object | From Damstra Forms API example response. |
| `fields.customTag.linked.href` | string | From Damstra Forms API example response. |
| `fields.customTag.linked.id` | number | From Damstra Forms API example response. |
| `fields.customTag.linked.signedHref` | string | From Damstra Forms API example response. |
| `fields.customTag.linked.type` | string | From Damstra Forms API example response. |
| `fields.customTag.linked.uuid` | string | From Damstra Forms API example response. |
| `fields.customTag.properties` | object | From Damstra Forms API example response. |
| `fields.customTag.properties.property1` | string | From Damstra Forms API example response. |
| `fields.customTag.properties.property2` | string | From Damstra Forms API example response. |
| `fields.customTag.signature` | object | From Damstra Forms API example response. |
| `fields.customTag.signature.contentType` | string | From Damstra Forms API example response. |
| `fields.customTag.signature.href` | string | From Damstra Forms API example response. |
| `fields.customTag.signature.id` | number | From Damstra Forms API example response. |
| `fields.customTag.signature.signedHref` | string | From Damstra Forms API example response. |
| `fields.customTag.signature.userId` | number | From Damstra Forms API example response. |
| `fields.customTag.value` | string | From Damstra Forms API example response. |
| `metadata` | object | From Damstra Forms API example response. |
| `metadata.children` | array<object> | From Damstra Forms API example response. |
| `metadata.children.href` | string | From Damstra Forms API example response. |
| `metadata.children.id` | number | From Damstra Forms API example response. |
| `metadata.children.pdfHref` | string | From Damstra Forms API example response. |
| `metadata.children.uuid` | string | From Damstra Forms API example response. |
| `metadata.createdAt` | date | From Damstra Forms API example response. |
| `metadata.creator` | object | From Damstra Forms API example response. |
| `metadata.creator.href` | string | From Damstra Forms API example response. |
| `metadata.creator.id` | number | From Damstra Forms API example response. |
| `metadata.creator.uuid` | string | From Damstra Forms API example response. |
| `metadata.href` | string | From Damstra Forms API example response. |
| `metadata.id` | number | From Damstra Forms API example response. |
| `metadata.owner` | object | From Damstra Forms API example response. |
| `metadata.owner.id` | number | From Damstra Forms API example response. |
| `metadata.owner.uuid` | string | From Damstra Forms API example response. |
| `metadata.project` | object | From Damstra Forms API example response. |
| `metadata.project.id` | number | From Damstra Forms API example response. |
| `metadata.project.uuid` | string | From Damstra Forms API example response. |
| `metadata.status` | number | From Damstra Forms API example response. |
| `metadata.template` | object | From Damstra Forms API example response. |
| `metadata.template.draftTemplate` | object | From Damstra Forms API example response. |
| `metadata.template.draftTemplate.href` | string | From Damstra Forms API example response. |
| `metadata.template.draftTemplate.id` | number | From Damstra Forms API example response. |
| `metadata.template.href` | string | From Damstra Forms API example response. |
| `metadata.template.id` | number | From Damstra Forms API example response. |
| `metadata.type` | string | From Damstra Forms API example response. |
| `metadata.updatedAt` | date | From Damstra Forms API example response. |
| `metadata.uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /forms/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-integration-representation.md) for the provider-specific parameters and requirements.

