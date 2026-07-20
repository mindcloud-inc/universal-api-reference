# Reteach: Get Customer Group



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-group?connectionId=$CONNECTION_ID&customerGroupId=7c78fa51-185c-47a5-b233-687e4a8b556e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerGroupId": "7c78fa51-185c-47a5-b233-687e4a8b556e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-group?${params}`, {
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
| `customerGroupId` | string | yes | The id of the customer group. Default: `7c78fa51-185c-47a5-b233-687e4a8b556e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "notificationMail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `notificationMail` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /v1/customer-group/{customerGroupId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-group.md) for the provider-specific parameters and requirements.

