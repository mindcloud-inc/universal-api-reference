# Pirsonal: Create Template

Creates a new template in Pirsonal.

```
POST https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | object | yes | TemplateNew_t object to create. |

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
| `response` | string | Created template ID returned by Pirsonal. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

