# Jotform: Create Form

Creates a form in Jotform.

```
POST https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | no | Form properties payload. |
| `questions` | object | no | Form questions payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `POST /user/forms` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

