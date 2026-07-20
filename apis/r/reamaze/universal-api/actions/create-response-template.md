# Reamaze: Create Response Template



```
POST https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-response-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-response-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "responseTemplate": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/create-response-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "responseTemplate": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseTemplate` | object | yes | Body payload field documented on https://www.reamaze.com/api/post_response_template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "id": 1,
      "name": "Ava Chen",
      "responseTemplateGroup": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `id` | number |  |
| `name` | string |  |
| `responseTemplateGroup` | object |  |

## Native endpoint

Through the native Reamaze API, this operation is `POST /response_templates` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-response-template.md) for the provider-specific parameters and requirements.

