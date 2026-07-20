# TxtSync: List Contacts

Retrieves contacts from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-contacts?${params}`, {
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
      "AddressLine1": "string",
      "AddressLine2": "string",
      "AllowSMS": true,
      "City": "string",
      "CompanyName": "Ava Chen",
      "ContactID": 1,
      "Country": "string",
      "CountryCode": "string",
      "County": "string",
      "CreatedBy": 1,
      "CreatedByApp": 1,
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "DateOfBirth": "2026-05-07T12:00:00.000Z",
      "EmailAddress": "ava@example.com",
      "ExternalReference": "string",
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "LastCommunicationDate": "2026-05-07T12:00:00.000Z",
      "LastName": "Chen",
      "LatestInboundSMSID": 1,
      "LatestOutboundSMSID": 1,
      "LatestSMSID": 1,
      "MobileNumber": "string",
      "MobileNumberCountryCode": "string",
      "ModifiedBy": 1,
      "ModifiedByApp": 1,
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "OverallRating": 1,
      "Postcode": "string",
      "Source": 1,
      "TotalDistinctLinkClicks": 1,
      "TotalFailedSMS": 1,
      "TotalInboundSMS": 1,
      "TotalLinksSent": 1,
      "TotalOutboundSMS": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressLine1` | string |  |
| `AddressLine2` | string |  |
| `AllowSMS` | boolean |  |
| `City` | string |  |
| `CompanyName` | string |  |
| `ContactID` | number |  |
| `Country` | string |  |
| `CountryCode` | string |  |
| `County` | string |  |
| `CreatedBy` | number |  |
| `CreatedByApp` | number |  |
| `CreatedDate` | date |  |
| `DateOfBirth` | date |  |
| `EmailAddress` | string |  |
| `ExternalReference` | string |  |
| `FirstName` | string |  |
| `FullName` | string |  |
| `LastCommunicationDate` | date |  |
| `LastName` | string |  |
| `LatestInboundSMSID` | number |  |
| `LatestOutboundSMSID` | number |  |
| `LatestSMSID` | number |  |
| `MobileNumber` | string |  |
| `MobileNumberCountryCode` | string |  |
| `ModifiedBy` | number |  |
| `ModifiedByApp` | number |  |
| `ModifiedDate` | date |  |
| `OverallRating` | number |  |
| `Postcode` | string |  |
| `Source` | number |  |
| `TotalDistinctLinkClicks` | number |  |
| `TotalFailedSMS` | number |  |
| `TotalInboundSMS` | number |  |
| `TotalLinksSent` | number |  |
| `TotalOutboundSMS` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /contacts` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

