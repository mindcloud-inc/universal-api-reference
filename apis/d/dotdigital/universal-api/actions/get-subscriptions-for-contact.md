# Dotdigital: Get Subscriptions for Contact

Retrieves subscriptions for a contact from Dotdigital.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-subscriptions-for-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-subscriptions-for-contact?connectionId=$CONNECTION_ID&email=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "john@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-subscriptions-for-contact?${params}`, {
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
| `email` | string | yes | Example: `john@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "email": "ava@example.com",
        "emailType": "ava@example.com",
        "id": 1,
        "optInType": "string",
        "status": "string"
      },
      "marketingPreferenceOptIns": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `contact.email` | string |  |
| `contact.emailType` | string |  |
| `contact.id` | number |  |
| `contact.optInType` | string |  |
| `contact.status` | string |  |
| `marketingPreferenceOptIns` | array<object> |  |

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/contacts/:email/subscriptions` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriptions-for-contact.md) for the provider-specific parameters and requirements.

