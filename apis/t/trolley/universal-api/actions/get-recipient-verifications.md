# Trolley: Get Recipient Verifications

Retrieves recipient verification results from Trolley.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-verifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-verifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/get-recipient-verifications?${params}`, {
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
| `recipientId` | string | no | Recipient ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business": [
        {}
      ],
      "individual": [
        {}
      ],
      "ok": true,
      "phone": [
        {}
      ],
      "watchlist": [
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
| `business` | array<object> |  |
| `individual` | array<object> |  |
| `ok` | boolean |  |
| `phone` | array<object> |  |
| `watchlist` | array<object> |  |

## Native endpoint

Through the native Trolley API, this operation is `POST /v1/verifications/get` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient-verifications.md) for the provider-specific parameters and requirements.

