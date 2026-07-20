# Google Forms: Update Form Info

Updates a form's title or description in Google Forms.

```
PUT https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/update-form-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/update-form-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/update-form-info', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form identifier. |
| `title` | string | no | New visible form title. Include this or Description. |
| `description` | string | no | New form description. Include this or Title. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Comma-separated Info fields to update, such as title,description. Defaults from provided fields when omitted. |
| `includeFormInResponse` | boolean | no | Return the updated form in the response. |
| `targetRevisionId` | string | no | Optional optimistic write-control revision ID; Google will transform against later edits when possible. |
| `requiredRevisionId` | string | no | Optional strict write-control revision ID; request fails if it is not current. |

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

Through the native Google Forms API, this operation is `POST /:formId:batchUpdate` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-info.md) for the provider-specific parameters and requirements.

