# Password.link: Create Secret Request



```
POST https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password.link `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordlink/latest/actions/create-secret-request', {
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
| `description` | string | no | Description for the Secret Request. |
| `message` | string | no | Message for the Secret Request viewer. |
| `expiration` | number | no | Expiration time for the Secret Request, in hours. |
| `limit` | number | no | Usage limit for the Secret Request. |
| `sendRequestToEmail` | string | no | Send the created Secret Request link to the given email address. |
| `sendToEmail` | string | no | Send the created Secret link created using the Secret Request to the given email address. |
| `secretDescription` | string | no | Description for the Secret created using the Secret Request. |
| `secretMessage` | string | no | Message for the Secret created using the Secret Request. |
| `secretExpiration` | number | no | Expiration time for the Secret created using the Secret Request, in hours. |
| `secretPassword` | string | no | Password for the Secret created using the Secret Request, in hours. |
| `secretMaxViews` | number | no | Maximum views for the Secret created using the Secret Request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created secret request ID. |

## Native endpoint

Through the native Password.link API, this operation is `POST /secret_requests` (base URL `https://password.link/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-secret-request.md) for the provider-specific parameters and requirements.

