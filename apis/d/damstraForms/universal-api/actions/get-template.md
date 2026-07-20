# Damstra Forms: Get Template

Retrieves a template from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-template?${params}`, {
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
| `id` | number | yes | The unique identifier of the template. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showManaged` | boolean | no | Determines whether to include integrated templates in the response. Default: `false`. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {
        "controlType": 1,
        "displayName": "Ava Chen",
        "exampleValue": "string",
        "fieldType": 1,
        "integrationTag": "string",
        "reference": "string",
        "sectionIndex": 1
      },
      "metadata": {
        "active": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "draftTemplate": {
          "href": "string",
          "id": 1
        },
        "href": "string",
        "id": 1,
        "name": "Ava Chen",
        "publishedVersion": 1,
        "sections": {
          "name": "Ava Chen"
        },
        "templateType": 1,
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | From Damstra Forms API example response. |
| `fields.controlType` | number | From Damstra Forms API example response. |
| `fields.displayName` | string | From Damstra Forms API example response. |
| `fields.exampleValue` | string | From Damstra Forms API example response. |
| `fields.fieldType` | number | From Damstra Forms API example response. |
| `fields.integrationTag` | string | From Damstra Forms API example response. |
| `fields.reference` | string | From Damstra Forms API example response. |
| `fields.sectionIndex` | number | From Damstra Forms API example response. |
| `metadata` | object | From Damstra Forms API example response. |
| `metadata.active` | boolean | From Damstra Forms API example response. |
| `metadata.createdAt` | date | From Damstra Forms API example response. |
| `metadata.draftTemplate` | object | From Damstra Forms API example response. |
| `metadata.draftTemplate.href` | string | From Damstra Forms API example response. |
| `metadata.draftTemplate.id` | number | From Damstra Forms API example response. |
| `metadata.href` | string | From Damstra Forms API example response. |
| `metadata.id` | number | From Damstra Forms API example response. |
| `metadata.name` | string | From Damstra Forms API example response. |
| `metadata.publishedVersion` | number | From Damstra Forms API example response. |
| `metadata.sections` | array<object> | From Damstra Forms API example response. |
| `metadata.sections.name` | string | From Damstra Forms API example response. |
| `metadata.templateType` | number | From Damstra Forms API example response. |
| `metadata.type` | string | From Damstra Forms API example response. |
| `metadata.updatedAt` | date | From Damstra Forms API example response. |
| `metadata.version` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /templates/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

