# FillFaster: Get Form Fields

Retrieves form fields from FillFaster by form ID.

```
GET https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-form-fields?connectionId=$CONNECTION_ID&formUID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formUID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/get-form-fields?${params}`, {
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
| `formUID` | string | yes | FillFaster form identifier to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "headers": [
        "string"
      ],
      "inputType": "string",
      "label": "string",
      "mapName": "Ava Chen",
      "name": "Ava Chen",
      "required": true,
      "validationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `headers` | array<string> | Column headers for table fields when present. |
| `inputType` | string | Field input type. |
| `label` | string | Field label. |
| `mapName` | string | Mapped integration variable name when present. |
| `name` | string | Field name. |
| `required` | boolean | Whether the field is required. |
| `validationType` | string | Field validation type. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/getFormFields` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-fields.md) for the provider-specific parameters and requirements.

