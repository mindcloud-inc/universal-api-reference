# Bitskout: Extract Data from Business Cards

Extracts business card data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-business-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-business-cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-business-cards', {
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
| `fileUrl` | string | no | Direct download URL for the business card image or document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "ADDRESS": "string",
        "COMPANY_NAME": "Ava Chen",
        "EMAIL_ADDRESS": "ava@example.com",
        "FAX": "string",
        "LOCATION": "string",
        "LOGO_URL": "https://example.com",
        "MOBILE": "string",
        "PERSON_NAME": "Ava Chen",
        "PERSON_POSITION": "string",
        "PHONE_NUMBER": "string",
        "RawJSON": "string",
        "WEBSITE": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Business card extraction outputs |
| `outputs.ADDRESS` | string | Address |
| `outputs.COMPANY_NAME` | string | Company Name |
| `outputs.EMAIL_ADDRESS` | string | Email |
| `outputs.FAX` | string | Fax |
| `outputs.LOCATION` | string | Location |
| `outputs.LOGO_URL` | string | Logo URL |
| `outputs.MOBILE` | string | Mobile phone number |
| `outputs.PERSON_NAME` | string | Person's name |
| `outputs.PERSON_POSITION` | string | Person's position |
| `outputs.PHONE_NUMBER` | string | Phone Number |
| `outputs.RawJSON` | string | Raw JSON |
| `outputs.WEBSITE` | string | Website URL |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/business_cards` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-business-cards.md) for the provider-specific parameters and requirements.

