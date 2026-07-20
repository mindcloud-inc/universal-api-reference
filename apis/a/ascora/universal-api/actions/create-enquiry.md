# Ascora: Create Enquiry

Creates a new enquiry in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-enquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-enquiry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-enquiry', {
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
| `companyName` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `mobile` | string | no |  |
| `phone` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `addressSuburb` | string | no |  |
| `addressState` | string | no |  |
| `addressPostcode` | string | no |  |
| `addressCountry` | string | no |  |
| `enquiryDescription` | string | no |  |
| `leadSource` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityId` | string | ID of the newly created enquiry. |
| `success` | boolean | Whether Ascora created the enquiry. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Enquiry` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enquiry.md) for the provider-specific parameters and requirements.

