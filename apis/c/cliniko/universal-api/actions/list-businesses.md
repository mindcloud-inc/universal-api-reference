# Cliniko: List Businesses

Retrieves businesses from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-businesses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-businesses?${params}`, {
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
      "businesses": [
        {
          "additionalInformation": {},
          "additionalInvoiceInformation": {},
          "address1": {},
          "address2": {},
          "appointmentRemindersEnabled": true,
          "appointments": {
            "links": {
              "self": "https://example.com"
            }
          },
          "appointmentTypeIds": [
            "string"
          ],
          "archivedAt": {},
          "businessName": "Ava Chen",
          "businessRegistrationName": {},
          "businessRegistrationValue": {},
          "city": {},
          "contactInformation": {},
          "country": "string",
          "countryCode": "string",
          "createdAt": "string",
          "deletedAt": {},
          "displayName": {},
          "emailReplyTo": {},
          "id": "string",
          "label": "string",
          "links": {
            "self": "https://example.com"
          },
          "postCode": {},
          "practitioners": {
            "links": {
              "self": "https://example.com"
            }
          },
          "showInOnlineBookings": true,
          "state": {},
          "timeZone": "string",
          "timeZoneIdentifier": "string",
          "updatedAt": "string",
          "websiteAddress": {}
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businesses[].additionalInformation` | object |  |
| `businesses[].additionalInvoiceInformation` | object |  |
| `businesses[].address1` | object |  |
| `businesses[].address2` | object |  |
| `businesses[].appointmentRemindersEnabled` | boolean |  |
| `businesses[].appointments.links.self` | string |  |
| `businesses[].appointmentTypeIds[]` | string |  |
| `businesses[].archivedAt` | object |  |
| `businesses[].businessName` | string |  |
| `businesses[].businessRegistrationName` | object |  |
| `businesses[].businessRegistrationValue` | object |  |
| `businesses[].city` | object |  |
| `businesses[].contactInformation` | object |  |
| `businesses[].country` | string |  |
| `businesses[].countryCode` | string |  |
| `businesses[].createdAt` | string |  |
| `businesses[].deletedAt` | object |  |
| `businesses[].displayName` | object |  |
| `businesses[].emailReplyTo` | object |  |
| `businesses[].id` | string |  |
| `businesses[].label` | string |  |
| `businesses[].links.self` | string |  |
| `businesses[].postCode` | object |  |
| `businesses[].practitioners.links.self` | string |  |
| `businesses[].showInOnlineBookings` | boolean |  |
| `businesses[].state` | object |  |
| `businesses[].timeZone` | string |  |
| `businesses[].timeZoneIdentifier` | string |  |
| `businesses[].updatedAt` | string |  |
| `businesses[].websiteAddress` | object |  |
| `links.self` | string |  |
| `totalEntries` | number |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /businesses` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

