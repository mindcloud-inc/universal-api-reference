# Resend: Create Audience

Creates a new audience in Resend.

```
POST https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-audience', {
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
| `name` | string | no | The name of the audience to create Example: `Registered Users`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Audience identifier. |
| `name` | string | Audience name. |
| `object` | string | Object type identifier. |

## Native endpoint

Through the native Resend API, this operation is `POST /audiences` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audience.md) for the provider-specific parameters and requirements.

