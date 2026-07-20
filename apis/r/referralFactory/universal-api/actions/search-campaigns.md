# Referral Factory: Search Campaigns

Finds campaigns in Referral Factory by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Factory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "assets": {},
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "ends_at": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": 1,
      "lang": "string",
      "name": "Ava Chen",
      "starts_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets` | object | Campaign visual assets such as logo, favicon, and QR code. |
| `code` | string | Campaign code. |
| `created_at` | date | Campaign creation date. |
| `ends_at` | date | Campaign end date. |
| `fields` | object | Campaign referrer and invitee field definitions. |
| `id` | number | Referral Factory campaign identifier. |
| `lang` | string | Campaign language. |
| `name` | string | Campaign name. |
| `starts_at` | date | Campaign start date. |
| `status` | string | Campaign status. |
| `url` | string | Public campaign URL. |

## Native endpoint

Through the native Referral Factory API, this operation is `POST /campaigns/search` (base URL `https://referral-factory.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-campaigns.md) for the provider-specific parameters and requirements.

