# Routee: Retrieve statistics for an email address by campaigns

Retrieves statistics for an email address by campaigns from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-an-email-address-by-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-an-email-address-by-campaigns?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-an-email-address-by-campaigns?${params}`, {
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
| `email` | string | yes | email address to retrieve statistics |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklist": true,
      "statistic": {
        "link": 1,
        "open": 1,
        "sent": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklist` | boolean |  |
| `statistic` | object |  |
| `statistic.link` | number |  |
| `statistic.open` | number |  |
| `statistic.sent` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /emails/:email/campaigns` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-statistics-for-an-email-address-by-campaigns.md) for the provider-specific parameters and requirements.

