# CalendarHero: Get Providers

Retrieves providers from CalendarHero.

```
GET https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/get-providers?${params}`, {
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
      "auth": {},
      "calendar": {},
      "categoryType": [
        "string"
      ],
      "contacts": {},
      "dateAdded": "string",
      "dateLastImport": "string",
      "dateUpdated": "string",
      "eAuth": "string",
      "faq": {},
      "group": {},
      "mail": {},
      "name": "Ava Chen",
      "orgId": "string",
      "providerType": "string",
      "rooms": {},
      "userId": "string",
      "xref": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `calendar` | object |  |
| `categoryType` | array<string> |  |
| `contacts` | object |  |
| `dateAdded` | string |  |
| `dateLastImport` | string |  |
| `dateUpdated` | string |  |
| `eAuth` | string |  |
| `faq` | object |  |
| `group` | object |  |
| `mail` | object |  |
| `name` | string |  |
| `orgId` | string |  |
| `providerType` | string |  |
| `rooms` | object |  |
| `userId` | string |  |
| `xref` | string |  |

## Native endpoint

Through the native CalendarHero API, this operation is `GET /provider` (base URL `https://api.calendarhero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-providers.md) for the provider-specific parameters and requirements.

