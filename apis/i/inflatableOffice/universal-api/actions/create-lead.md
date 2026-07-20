# InflatableOffice: Create Lead

Creates a new lead in InflatableOffice.

```
POST https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-lead', {
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
| `additionalnotes1` | string | no |  |
| `additionalnotes2` | string | no |  |
| `adjust` | string | no |  |
| `coupon_code` | string | no |  |
| `customerid` | string | no |  |
| `deliverytype` | string | no |  |
| `distcharge` | string | no |  |
| `eventcity` | string | no |  |
| `eventcountry` | string | no |  |
| `eventduration` | string | no |  |
| `eventenddate_text` | string | no |  |
| `eventendtime` | string | no |  |
| `eventendtime_text` | string | no |  |
| `eventname` | string | no |  |
| `eventstartdate_text` | string | no |  |
| `eventstarttime` | string | no |  |
| `eventstarttime_text` | string | no |  |
| `eventstate` | string | no |  |
| `eventstreet` | string | no |  |
| `eventzip` | string | no |  |
| `fee` | string | no |  |
| `guests` | string | no |  |
| `locationid` | string | no |  |
| `notes` | string | no |  |
| `recalculate` | string | no |  |
| `referral` | string | no |  |
| `rental_names` | string | no |  |
| `salestax` | string | no |  |
| `staffcost` | string | no |  |
| `status` | string | no |  |
| `surface` | string | no |  |
| `taxexempt` | string | no |  |
| `taxrate` | string | no |  |
| `venuecontact` | string | no |  |
| `venuename` | string | no |  |
| `venuenotes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "recordid": "string",
      "requestTime": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider result message. |
| `recordid` | string | Created lead ID. |
| `requestTime` | number | Provider request timestamp. |
| `status` | number | HTTP status code returned by InflatableOffice. |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /leads` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

