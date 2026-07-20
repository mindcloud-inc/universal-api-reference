# SignRequest: Resend SignRequest



```
PUT https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/resend-sign-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/resend-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "38525278-876a-4f53-a69c-db39e82c753f"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/resend-sign-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "38525278-876a-4f53-a69c-db39e82c753f"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID of the SignRequest to resend Example: `38525278-876a-4f53-a69c-db39e82c753f`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detail` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `POST /signrequests/:uuid/resend_signrequest_email/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-sign-request.md) for the provider-specific parameters and requirements.

