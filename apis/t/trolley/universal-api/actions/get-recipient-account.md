# Trolley: Get Recipient Account

Retrieves a recipient payment account from Trolley.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-account?connectionId=$CONNECTION_ID&id=string&recipientAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "recipientAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-account?${params}`, {
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
| `id` | string | yes |  |
| `recipientAccountId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Trolley API, this operation is `GET /v1/recipients/:id/accounts/:recipientAccountId` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient-account.md) for the provider-specific parameters and requirements.

