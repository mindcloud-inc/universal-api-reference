# LoginRadius: List Webhook Configurations

Retrieves webhook configurations from your LoginRadius tenant.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-webhook-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-webhook-configurations?connectionId=$CONNECTION_ID&accessToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-webhook-configurations?${params}`, {
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
| `accessToken` | string | yes | Bearer access token authorized to list webhook configurations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Data` | array<object> | Webhook configuration records returned by LoginRadius. |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /v2/manage/webhooks` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-configurations.md) for the provider-specific parameters and requirements.

