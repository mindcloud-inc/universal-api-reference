# Deftform: List Form Fields

Retrieves fields for a form from Deftform.

```
GET https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-fields?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-form-fields?${params}`, {
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
| `formId` | string | yes | The Deftform form ID, available from the form detail page or the List Forms action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "mandatory": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Field label. |
| `mandatory` | boolean | Whether the field is mandatory. |
| `uuid` | string | Stable field UUID used when submitting response data. |

## Native endpoint

Through the native Deftform API, this operation is `GET /forms/:formId/fields` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-fields.md) for the provider-specific parameters and requirements.

