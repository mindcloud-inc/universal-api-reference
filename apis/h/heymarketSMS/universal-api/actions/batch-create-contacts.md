# Heymarket SMS: Batch Create Contacts



```
POST https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/batch-create-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/batch-create-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/batch-create-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Array of contacts to create. |
| `contacts[].first` | string | no | First name. |
| `contacts[].last` | string | no | Last name. |
| `contacts[].displayName` | string | no | Display name. |
| `contacts[].phone` | string | no | Phone number in E.164 format without the plus sign. |
| `contacts[].email` | string | no | Email address. |
| `contacts[].isOptedOut` | boolean | no | Whether the contact is opted out of messaging. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `overwrite` | boolean | no | Overwrite matching existing contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `POST /v1/batch/contacts` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-create-contacts.md) for the provider-specific parameters and requirements.

