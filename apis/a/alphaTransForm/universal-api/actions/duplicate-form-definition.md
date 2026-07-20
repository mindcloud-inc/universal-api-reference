# Alpha TransForm: Duplicate Form Definition

Creates a duplicate form definition in Alpha TransForm.

```
POST https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/duplicate-form-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/duplicate-form-definition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "newFormId": "string",
  "newFormName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/duplicate-form-definition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "newFormId": "string",
    "newFormName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | FormId of the form definition to be duplicated |
| `newFormId` | string | yes | FormId for the duplicated form definition |
| `newFormName` | string | yes | Friendly name for the duplicate form definition |
| `newAccountId` | string | no | Optional target account for the duplicated form definition |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formsAdded": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formsAdded` | number | Number of records added. |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /DuplicateFormDefinition` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-form-definition.md) for the provider-specific parameters and requirements.

