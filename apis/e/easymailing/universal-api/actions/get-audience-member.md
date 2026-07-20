# Easymailing: Get Audience Member

Retrieves an audience member from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience-member?connectionId=$CONNECTION_ID&audienceUuid=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "audienceUuid": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-audience-member?${params}`, {
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
| `audienceUuid` | string | yes | Audience UUID. |
| `uuid` | string | yes | Member UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audience": "string",
      "clientIp": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "groups": [
        {
          "color": "string",
          "description": "string",
          "public": true,
          "title": "string"
        }
      ],
      "id": 1,
      "locale": {},
      "location": {
        "city": {},
        "country": {},
        "countryCode": {},
        "lat": {},
        "lng": {},
        "postalCode": {},
        "timezone": {}
      },
      "memberConsent": {
        "consentAt": "2026-05-07T12:00:00.000Z",
        "ip": {}
      },
      "rating": 1,
      "source": "string",
      "stats": {
        "avgRevenue": 1,
        "clickRate": 1,
        "deliveredEmails": 1,
        "openRate": 1,
        "orderRate": 1,
        "orders": 1,
        "revenue": 1,
        "sent": 1,
        "uniqueClicks": 1,
        "uniqueOpens": 1
      },
      "status": "string",
      "suscriptionForm": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audience` | string |  |
| `clientIp` | object |  |
| `createdAt` | date |  |
| `email` | string |  |
| `groups[].color` | string |  |
| `groups[].description` | string |  |
| `groups[].public` | boolean |  |
| `groups[].title` | string |  |
| `id` | number |  |
| `locale` | object |  |
| `location.city` | object |  |
| `location.country` | object |  |
| `location.countryCode` | object |  |
| `location.lat` | object |  |
| `location.lng` | object |  |
| `location.postalCode` | object |  |
| `location.timezone` | object |  |
| `memberConsent.consentAt` | date |  |
| `memberConsent.ip` | object |  |
| `rating` | number |  |
| `source` | string |  |
| `stats.avgRevenue` | number |  |
| `stats.clickRate` | number |  |
| `stats.deliveredEmails` | number |  |
| `stats.openRate` | number |  |
| `stats.orderRate` | number |  |
| `stats.orders` | number |  |
| `stats.revenue` | number |  |
| `stats.sent` | number |  |
| `stats.uniqueClicks` | number |  |
| `stats.uniqueOpens` | number |  |
| `status` | string |  |
| `suscriptionForm` | object |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Easymailing API, this operation is `GET /audiences/{{audienceUuid}}/members/{{uuid}}` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience-member.md) for the provider-specific parameters and requirements.

