# InflatableOffice: List Leads

Retrieves leads from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-leads?${params}`, {
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
      "amountpaid": "string",
      "contactid": "string",
      "createtimeUtc": "string",
      "deliverytype": "string",
      "eventcity": "string",
      "eventcountry": "string",
      "eventduration": "string",
      "eventname": "Ava Chen",
      "eventorganization": "string",
      "eventstarttime": "string",
      "eventstarttimeUtc": "string",
      "eventstate": "string",
      "eventstreet": "string",
      "eventzip": "string",
      "href": "string",
      "id": "string",
      "modifiedtimeUtc": "string",
      "requestTime": 1,
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
| `amountpaid` | string |  |
| `contactid` | string |  |
| `createtimeUtc` | string |  |
| `deliverytype` | string |  |
| `eventcity` | string |  |
| `eventcountry` | string |  |
| `eventduration` | string |  |
| `eventname` | string |  |
| `eventorganization` | string |  |
| `eventstarttime` | string |  |
| `eventstarttimeUtc` | string |  |
| `eventstate` | string |  |
| `eventstreet` | string |  |
| `eventzip` | string |  |
| `href` | string |  |
| `id` | string |  |
| `modifiedtimeUtc` | string |  |
| `requestTime` | number |  |
| `statusid` | string |  |
| `surface` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /leads` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

