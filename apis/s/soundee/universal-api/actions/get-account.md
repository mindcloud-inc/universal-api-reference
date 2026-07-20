# Soundee: Get Account

Retrieves your Soundee producer account details.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account?${params}`, {
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
      "active": 1,
      "admin": 1,
      "avatar": {},
      "bio": "string",
      "color": "string",
      "country": {},
      "countryId": 1,
      "created": 1,
      "displayname": "Ava Chen",
      "email": "ava@example.com",
      "entityId": 1,
      "firstName": "Ava",
      "id": 1,
      "interaction": {},
      "isProducer": 1,
      "lastName": "Chen",
      "socials": [
        {}
      ],
      "subscription": {},
      "type": "string",
      "uploads": 1,
      "username": "Ava Chen",
      "vatNumber": "string",
      "verified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `admin` | number |  |
| `avatar` | object |  |
| `bio` | string |  |
| `color` | string |  |
| `country` | object |  |
| `countryId` | number |  |
| `created` | number |  |
| `displayname` | string |  |
| `email` | string |  |
| `entityId` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `interaction` | object |  |
| `isProducer` | number |  |
| `lastName` | string |  |
| `socials` | array<object> |  |
| `subscription` | object |  |
| `type` | string |  |
| `uploads` | number |  |
| `username` | string |  |
| `vatNumber` | string |  |
| `verified` | number |  |

## Native endpoint

Through the native Soundee API, this operation is `GET /` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

