# Zoho People: Get Form Fields

Retrieves fields for a Zoho People form.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-fields?connectionId=$CONNECTION_ID&formLinkName=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formLinkName": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-form-fields?${params}`, {
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
| `formLinkName` | string | yes | Zoho People formLinkName. Example: employee. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autofillvalue": "string",
      "comptype": "string",
      "description": "string",
      "descriptionType": 1,
      "displayname": "Ava Chen",
      "displayType": "string",
      "formcomponentid": 1,
      "ismandatory": true,
      "isPrimary": true,
      "labelname": "Ava Chen",
      "maxLength": 1,
      "options": {},
      "referedFieldId": 1,
      "referedFieldName": "Ava Chen",
      "referedFormId": 1,
      "referedFormName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autofillvalue` | string |  |
| `comptype` | string |  |
| `description` | string |  |
| `descriptionType` | number |  |
| `displayname` | string |  |
| `displayType` | string |  |
| `formcomponentid` | number |  |
| `ismandatory` | boolean |  |
| `isPrimary` | boolean |  |
| `labelname` | string |  |
| `maxLength` | number |  |
| `options` | object |  |
| `referedFieldId` | number |  |
| `referedFieldName` | string |  |
| `referedFormId` | number |  |
| `referedFormName` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/forms/:formLinkName/components` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-fields.md) for the provider-specific parameters and requirements.

