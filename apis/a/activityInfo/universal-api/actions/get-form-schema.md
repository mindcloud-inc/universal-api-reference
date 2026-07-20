# ActivityInfo: Get Form Schema

Retrieves a form schema from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-form-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-form-schema?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-form-schema?${params}`, {
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
| `formId` | string | yes | ActivityInfo form ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseId": "string",
      "elements": [
        {}
      ],
      "id": "string",
      "label": "string",
      "parentFormId": "string",
      "schemaVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | string | Owning database ID. |
| `elements` | array<object> | Form fields, section headers, and other elements. |
| `id` | string | Form ID. |
| `label` | string | Form label. |
| `parentFormId` | string | Parent form ID, when this is a subform. |
| `schemaVersion` | string | Server-assigned schema version. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/form/:formId/schema` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-schema.md) for the provider-specific parameters and requirements.

