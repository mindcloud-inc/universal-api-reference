# Cliniko: List Practitioners

Retrieves practitioners from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-practitioners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-practitioners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-practitioners?${params}`, {
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
      "links": {
        "self": "https://example.com"
      },
      "practitioners": [
        {
          "active": true,
          "appointments": {
            "links": {
              "self": "https://example.com"
            }
          },
          "appointmentTypes": {
            "links": {
              "self": "https://example.com"
            }
          },
          "createdAt": "string",
          "description": {},
          "designation": {},
          "displayName": "Ava Chen",
          "firstName": "Ava",
          "id": "string",
          "invoices": {
            "links": {
              "self": "https://example.com"
            }
          },
          "label": "string",
          "lastName": "Chen",
          "links": {
            "self": "https://example.com"
          },
          "practitionerReferenceNumbers": {
            "links": {
              "self": "https://example.com"
            }
          },
          "showInOnlineBookings": true,
          "title": {},
          "updatedAt": "string",
          "user": {
            "links": {
              "self": "https://example.com"
            }
          }
        }
      ],
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links.self` | string |  |
| `practitioners[].active` | boolean |  |
| `practitioners[].appointments.links.self` | string |  |
| `practitioners[].appointmentTypes.links.self` | string |  |
| `practitioners[].createdAt` | string |  |
| `practitioners[].description` | object |  |
| `practitioners[].designation` | object |  |
| `practitioners[].displayName` | string |  |
| `practitioners[].firstName` | string |  |
| `practitioners[].id` | string |  |
| `practitioners[].invoices.links.self` | string |  |
| `practitioners[].label` | string |  |
| `practitioners[].lastName` | string |  |
| `practitioners[].links.self` | string |  |
| `practitioners[].practitionerReferenceNumbers.links.self` | string |  |
| `practitioners[].showInOnlineBookings` | boolean |  |
| `practitioners[].title` | object |  |
| `practitioners[].updatedAt` | string |  |
| `practitioners[].user.links.self` | string |  |
| `totalEntries` | number |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /practitioners` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-practitioners.md) for the provider-specific parameters and requirements.

