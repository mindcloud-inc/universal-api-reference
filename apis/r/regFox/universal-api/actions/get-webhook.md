# RegFox: Get Webhook

Retrieves webhook details from the RegFox account.

```
GET https://connect.mindcloud.co/v1/universal/regFox/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RegFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/regFox/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | The RegFox webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "responseCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Webhook returned for the requested RegFox webhook ID. |
| `responseCode` | number | HTTP-style response code returned by Webconnex. |

## Native endpoint

Through the native RegFox API, this operation is `GET webhooks/{id}` (base URL `https://api.webconnex.com/v2/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

