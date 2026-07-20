# Routee: Add contacts to blacklist

Adds contacts to the blacklist in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-contacts-to-blacklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-contacts-to-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": "string",
  "contacts[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/add-contacts-to-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": "string",
    "contacts[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service` | string | yes | The service (Sms, Voice, Viber, TwoStep, Lookup, NumberValidator) for which the contact will be added in blacklist. |
| `contacts[]` | array<string> | yes | The contacts' ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updated` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /contacts/my/blacklist/:service` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-blacklist.md) for the provider-specific parameters and requirements.

