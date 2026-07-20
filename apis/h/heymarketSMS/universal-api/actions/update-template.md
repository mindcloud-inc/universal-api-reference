# Heymarket SMS: Update Template



```
PUT https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1,
  "title": "Codex Stage 3 Template",
  "content.text": "Updated template body"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1,
    "title": "Codex Stage 3 Template",
    "content.text": "Updated template body"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | yes | Unique identifier of the template. |
| `title` | string | yes | Template name. Example: `Codex Stage 3 Template`. |
| `content.text` | string | yes | Text content for the template body. Example: `Updated template body`. |
| `archived` | boolean | no | Whether the template should be archived. Default: `false`. |
| `localId` | string | no | Client unique identifier for the template. Example: `tmpl-002`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "rev": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `rev` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `PUT /v1/template/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

