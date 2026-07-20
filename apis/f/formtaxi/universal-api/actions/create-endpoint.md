# Form.taxi: Create Endpoint

Creates a new endpoint in Form.taxi.

```
POST https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/create-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.taxi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/create-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com",
  "formName": "Contact Form",
  "language": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formtaxi/latest/actions/create-endpoint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com",
    "formName": "Contact Form",
    "language": "en"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address used as the destination for form submissions and as the username for the new account. Example: `user@example.com`. |
| `formName` | string | yes | Name of the form to create. Example: `Contact Form`. |
| `language` | string | yes | Language for the account and email notifications. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteUrl` | string | no | Website where the form will be used. Example: `https://example.com`. |
| `timezone` | string | no | IANA time zone identifier for the account. Example: `Europe/Vienna`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endpoint_url": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoint_url` | string | The created Form.taxi endpoint URL. |
| `success` | boolean | Whether the endpoint creation succeeded. |

## Native endpoint

Through the native Form.taxi API, this operation is `POST /create-endpoint` (base URL `https://form.taxi/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-endpoint.md) for the provider-specific parameters and requirements.

