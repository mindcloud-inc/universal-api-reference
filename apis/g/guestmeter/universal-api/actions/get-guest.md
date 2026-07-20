# Guestmeter: Get Guest

Retrieves guest details from Guestmeter.

```
GET https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/get-guest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Guestmeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/get-guest?connectionId=$CONNECTION_ID&guestId=9d77b4cc-cdaa-4768-9aa9-94a0d772f222" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guestId": "9d77b4cc-cdaa-4768-9aa9-94a0d772f222"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/get-guest?${params}`, {
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
| `guestId` | string | yes | Guest ID in UUID format. Example: `9d77b4cc-cdaa-4768-9aa9-94a0d772f222`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickedDate": "string",
      "contactInfo": "string",
      "contactType": "string",
      "countryCode": "string",
      "creationDate": "string",
      "feedback": "string",
      "guestID": "string",
      "guestName": "Ava Chen",
      "integrationID": "string",
      "languageCode": "string",
      "mainChannel": "string",
      "propertyName": "Ava Chen",
      "ratedDate": "string",
      "rating": "string",
      "ratingType": "string",
      "roomNumber": "string",
      "sentDate": "string",
      "status": "string",
      "statusDetail": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickedDate` | string |  |
| `contactInfo` | string |  |
| `contactType` | string |  |
| `countryCode` | string |  |
| `creationDate` | string |  |
| `feedback` | string |  |
| `guestID` | string |  |
| `guestName` | string |  |
| `integrationID` | string |  |
| `languageCode` | string |  |
| `mainChannel` | string |  |
| `propertyName` | string |  |
| `ratedDate` | string |  |
| `rating` | string |  |
| `ratingType` | string |  |
| `roomNumber` | string |  |
| `sentDate` | string |  |
| `status` | string |  |
| `statusDetail` | string |  |

## Native endpoint

Through the native Guestmeter API, this operation is `GET /getGuest` (base URL `https://www.guestmeter.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-guest.md) for the provider-specific parameters and requirements.

