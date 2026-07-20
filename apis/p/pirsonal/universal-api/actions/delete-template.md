# Pirsonal: Delete Template

Deletes an existing template from Pirsonal.

```
DELETE https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/delete-template?connectionId=$CONNECTION_ID&templateID=string&removeExternalFiles=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateID": "string",
  "removeExternalFiles": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/delete-template?${params}`, {
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
| `templateID` | string | yes | ID of the template to delete. |
| `removeExternalFiles` | boolean | yes | Whether Pirsonal should remove external videos too, such as YouTube files. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Pirsonal delete response, normally OK. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

