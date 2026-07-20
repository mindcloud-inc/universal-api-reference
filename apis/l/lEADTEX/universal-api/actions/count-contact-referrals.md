# LEADTEX: Count Contact Referrals

Retrieves the total referrals in a contact's network in LEADTEX.

```
GET https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/count-contact-referrals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/count-contact-referrals?connectionId=$CONNECTION_ID&contact_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/count-contact-referrals?${params}`, {
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
| `contact_id` | number | yes | ID of the contact whose referral network should be counted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": 1,
      "errors": {},
      "message": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | number |  |
| `errors` | object |  |
| `message` | string |  |
| `total` | number |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /getCountReferrals?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-contact-referrals.md) for the provider-specific parameters and requirements.

