# Google Forms: Batch Update Form

Applies batch updates to a form in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/batch-update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/batch-update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/batch-update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `requests[]` | array<object> | yes | Raw Google Forms batchUpdate request objects. Use this for advanced updateFormInfo, updateSettings, createItem, moveItem, deleteItem, or updateItem calls. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeFormInResponse` | boolean | no | Return the updated form in the response. |
| `requiredRevisionId` | string | no | Strict write-control revision ID; request fails if it is not current. |
| `targetRevisionId` | string | no | Optimistic write-control revision ID; Google transforms against later edits when possible. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "writeControl": {
        "requiredRevisionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `writeControl.requiredRevisionId` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-form.md) for the provider-specific parameters and requirements.

