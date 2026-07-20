# InflatableOffice: Get Detailed Lead

Retrieves a lead with detailed fields from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-detailed-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-detailed-lead?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-detailed-lead?${params}`, {
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
| `leadId` | string | no |  |

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
      "organizationInfo": {},
      "payments": {},
      "rentals": [
        {}
      ],
      "requestTime": 1,
      "shifts": [
        {}
      ],
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
| `organizationInfo` | object |  |
| `payments` | object |  |
| `rentals` | array<object> |  |
| `requestTime` | number |  |
| `shifts` | array<object> |  |
| `status` | object |  |
| `statusid` | string |  |
| `surface` | string |  |
| `total` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /leads/:leadId` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-lead.md) for the provider-specific parameters and requirements.

