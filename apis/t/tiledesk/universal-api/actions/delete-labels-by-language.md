# Tiledesk: Delete Labels By Language

Deletes labels for a language from Tiledesk.

```
DELETE https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-labels-by-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-labels-by-language?connectionId=$CONNECTION_ID&lang=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lang": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/delete-labels-by-language?${params}`, {
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
| `lang` | string | yes | The label language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lang": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lang` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tiledesk API, this operation is `DELETE /{{credentials.projectId}}/labels/:lang` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-labels-by-language.md) for the provider-specific parameters and requirements.

