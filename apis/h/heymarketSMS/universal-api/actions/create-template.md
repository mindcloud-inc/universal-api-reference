# Heymarket SMS: Create Template



```
POST https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Welcome Template",
  "content.text": "Hey {{first_name}}, thanks for reaching out."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Welcome Template",
    "content.text": "Hey {{first_name}}, thanks for reaching out."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Template name. Example: `Welcome Template`. |
| `content.text` | string | yes | Text content for the template body. Example: `Hey {{first_name}}, thanks for reaching out.`. |
| `archived` | boolean | no | Whether the template should be archived. Default: `false`. |
| `localId` | string | no | Client unique identifier for the template. Example: `tmpl-001`. |

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

Through the native Heymarket SMS API, this operation is `POST /v1/template` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

