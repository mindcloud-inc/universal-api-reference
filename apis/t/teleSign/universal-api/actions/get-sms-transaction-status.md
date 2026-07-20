# TeleSign: Get SMS Transaction Status



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-sms-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-sms-transaction-status?connectionId=$CONNECTION_ID&referenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "referenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-sms-transaction-status?${params}`, {
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
| `referenceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string | External transaction ID when provided. |
| `reference_id` | string | TeleSign reference ID. |
| `status.code` | number | Provider status code. |
| `status.description` | string | Provider status description. |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v1/messaging/{reference_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-transaction-status.md) for the provider-specific parameters and requirements.

