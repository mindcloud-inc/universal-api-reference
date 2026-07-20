# Guestmeter: List Guests

Retrieves guests from Guestmeter.

```
GET https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Guestmeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests?${params}`, {
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

Through the native Guestmeter API, this operation is `GET /getGuestList` (base URL `https://www.guestmeter.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guests.md) for the provider-specific parameters and requirements.

