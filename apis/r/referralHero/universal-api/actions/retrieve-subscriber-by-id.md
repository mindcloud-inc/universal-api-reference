# ReferralHero: Retrieve Subscriber by ID

Retrieves a subscriber from ReferralHero by ID.

```
GET https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/retrieve-subscriber-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/retrieve-subscriber-by-id?connectionId=$CONNECTION_ID&subscriberId=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/retrieve-subscriber-by-id?${params}`, {
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
| `subscriberId` | string | yes | Subscriber ID. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "id": "string",
      "lastUpdatedAt": 1,
      "name": "Ava Chen",
      "response": "string",
      "universalLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `id` | string |  |
| `lastUpdatedAt` | number |  |
| `name` | string |  |
| `response` | string |  |
| `universalLink` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `GET /lists/:uuid/subscribers/:subscriber_id` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscriber-by-id.md) for the provider-specific parameters and requirements.

