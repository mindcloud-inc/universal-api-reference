# Routee: Retrieve statistics for email addresses by campaigns and presence in lists

Retrieves statistics for email addresses by campaigns and presence in lists from Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | no | array of contacts ["example@yourdomain.com", "example2@yourdomain.com"] |

## Response

```json
{
  "success": true,
  "data": [
    {
      "example@yourdomain": {
        "com": {
          "adressbooks": [
            [
              {}
            ]
          ],
          "blacklist": true,
          "link": 1,
          "open": 1,
          "sent": 1
        }
      },
      "example2@yourdomain": {
        "com": {
          "adressbooks": [
            [
              {}
            ]
          ],
          "blacklist": true,
          "link": 1,
          "open": 1,
          "sent": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `example@yourdomain.com` | object |  |
| `example@yourdomain.com.adressbooks[]` | array<object> |  |
| `example@yourdomain.com.adressbooks[].id` | number |  |
| `example@yourdomain.com.adressbooks[].name` | string |  |
| `example@yourdomain.com.blacklist` | boolean |  |
| `example@yourdomain.com.link` | number |  |
| `example@yourdomain.com.open` | number |  |
| `example@yourdomain.com.sent` | number |  |
| `example2@yourdomain.com` | object |  |
| `example2@yourdomain.com.adressbooks[]` | array<object> |  |
| `example2@yourdomain.com.adressbooks[].id` | number |  |
| `example2@yourdomain.com.adressbooks[].name` | string |  |
| `example2@yourdomain.com.blacklist` | boolean |  |
| `example2@yourdomain.com.link` | number |  |
| `example2@yourdomain.com.open` | number |  |
| `example2@yourdomain.com.sent` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /emails/campaigns` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists.md) for the provider-specific parameters and requirements.

