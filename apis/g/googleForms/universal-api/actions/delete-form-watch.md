# Google Forms: Delete Form Watch

Deletes an existing form watch from Google Forms.

```
DELETE https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/delete-form-watch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/delete-form-watch?connectionId=$CONNECTION_ID&formId=string&watchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "watchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleForms/latest/actions/delete-form-watch?${params}`, {
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
| `formId` | string | yes | The form identifier. |
| `watchId` | string | yes | The watch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "error": {
        "code": "string",
        "message": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `error.code` | string |  |
| `error.message` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Google Forms API, this operation is `DELETE /:formId/watches/:watchId` (base URL `https://forms.googleapis.com/v1/forms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form-watch.md) for the provider-specific parameters and requirements.

