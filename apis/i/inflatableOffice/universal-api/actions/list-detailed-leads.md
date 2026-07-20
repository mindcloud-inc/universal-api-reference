# InflatableOffice: List Detailed Leads

Retrieves leads with detailed fields from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-leads?${params}`, {
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
      "amountpaid": 1,
      "contactid": "string",
      "cust": {},
      "deliverytype": "string",
      "eventcity": "string",
      "eventcountry": "string",
      "eventendtime": "string",
      "eventname": "Ava Chen",
      "eventorganization": "string",
      "eventstarttime": "string",
      "eventstate": "string",
      "eventstreet": "string",
      "eventzip": "string",
      "href": "string",
      "id": "string",
      "payments": {},
      "rentals": [
        {}
      ],
      "requestTime": 1,
      "status": {},
      "statusid": "string",
      "surface": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountpaid` | number |  |
| `contactid` | string |  |
| `cust` | object |  |
| `deliverytype` | string |  |
| `eventcity` | string |  |
| `eventcountry` | string |  |
| `eventendtime` | string |  |
| `eventname` | string |  |
| `eventorganization` | string |  |
| `eventstarttime` | string |  |
| `eventstate` | string |  |
| `eventstreet` | string |  |
| `eventzip` | string |  |
| `href` | string |  |
| `id` | string |  |
| `payments` | object |  |
| `rentals` | array<object> |  |
| `requestTime` | number |  |
| `status` | object |  |
| `statusid` | string |  |
| `surface` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /leads` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-detailed-leads.md) for the provider-specific parameters and requirements.

