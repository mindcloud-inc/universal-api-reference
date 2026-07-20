# Cloudmersive Data Validation: Check IP Bot Status

Checks whether an IP is a bot client.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-bot-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-bot-status?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-ip-bot-status?${params}`, {
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
| `value` | string | yes | IP address to check for bot status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IsBot": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IsBot` | boolean |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/ip/is-bot` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-ip-bot-status.md) for the provider-specific parameters and requirements.

