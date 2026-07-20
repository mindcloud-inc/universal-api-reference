# Contacts+: Get Account

Retrieves current account details from Contacts+.

```
GET https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account?${params}`, {
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
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "emails": [
        {
          "type": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "profileData": {
        "name": {
          "familyName": "Ava Chen",
          "givenName": "Ava Chen"
        },
        "photos": [
          {
            "type": "string",
            "value": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | date |  |
| `emails[].type` | string |  |
| `emails[].value` | string |  |
| `profileData.name.familyName` | string |  |
| `profileData.name.givenName` | string |  |
| `profileData.photos[].type` | string |  |
| `profileData.photos[].value` | string |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/account.get` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

