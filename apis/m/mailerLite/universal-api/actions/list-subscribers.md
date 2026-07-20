# MailerLite: List Subscribers

Retrieves a page of subscribers from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-subscribers?${params}`, {
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
| `limit` | number | no | Number of subscribers per page (up to 100). Default: `25`. |
| `page` | number | no | Page number to fetch. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickRate": 1,
      "clicksCount": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "fields": {
        "city": {},
        "company": {},
        "country": {},
        "lastName": {},
        "mcField20260302202529": {},
        "mcField20260302202809": {},
        "mcField20260302203026": {},
        "mcField20260302203214": {},
        "mcField20260302203521": {},
        "mcField20260302203754": {},
        "mcField20260302204008": {},
        "mcField20260302204855": {},
        "name": {},
        "phone": {},
        "state": {},
        "zIP": {}
      },
      "id": "string",
      "ipAddress": {},
      "openRate": 1,
      "opensCount": 1,
      "optedInAt": {},
      "optinIp": {},
      "sent": 1,
      "source": "string",
      "status": "string",
      "subscribedAt": "string",
      "unsubscribedAt": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickRate` | number |  |
| `clicksCount` | number |  |
| `createdAt` | string |  |
| `email` | string |  |
| `fields.city` | object |  |
| `fields.company` | object |  |
| `fields.country` | object |  |
| `fields.lastName` | object |  |
| `fields.mcField20260302202529` | object |  |
| `fields.mcField20260302202809` | object |  |
| `fields.mcField20260302203026` | object |  |
| `fields.mcField20260302203214` | object |  |
| `fields.mcField20260302203521` | object |  |
| `fields.mcField20260302203754` | object |  |
| `fields.mcField20260302204008` | object |  |
| `fields.mcField20260302204855` | object |  |
| `fields.name` | object |  |
| `fields.phone` | object |  |
| `fields.state` | object |  |
| `fields.zIP` | object |  |
| `id` | string |  |
| `ipAddress` | object |  |
| `openRate` | number |  |
| `opensCount` | number |  |
| `optedInAt` | object |  |
| `optinIp` | object |  |
| `sent` | number |  |
| `source` | string |  |
| `status` | string |  |
| `subscribedAt` | string |  |
| `unsubscribedAt` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /subscribers` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

