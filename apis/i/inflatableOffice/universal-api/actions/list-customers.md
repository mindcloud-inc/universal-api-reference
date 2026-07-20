# InflatableOffice: List Customers

Retrieves customers from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers?${params}`, {
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
| `body` | boolean | no | When true, returns more customer details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aataxexempt": "string",
      "active": "string",
      "address2": "string",
      "cellphone": "string",
      "city": "string",
      "country": "string",
      "createtime": "string",
      "createtimeTs": "string",
      "createtimeUtc": "string",
      "customertype": "string",
      "email": "ava@example.com",
      "fax": "string",
      "fbprofileid": "string",
      "firstname": "Ava",
      "homephone": "string",
      "href": "string",
      "id": "string",
      "isblacklisted": "string",
      "lastactiontime": "string",
      "lastcontacttime": "string",
      "lastname": "Chen",
      "locationid": "string",
      "modifiedtime": "string",
      "modifiedtimeTs": "string",
      "modifiedtimeUtc": "string",
      "notes": "string",
      "officephone": "string",
      "oktotext": "string",
      "organization": "string",
      "qboid": "string",
      "qboname": "Ava Chen",
      "qbosendinvoice": "string",
      "qbosynctoken": "string",
      "qboupdatetime": "string",
      "referral": "string",
      "repeatcustomer": "string",
      "score": "string",
      "state": "string",
      "street": "string",
      "taxexemptid": "string",
      "title": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aataxexempt` | string |  |
| `active` | string |  |
| `address2` | string |  |
| `cellphone` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createtime` | string |  |
| `createtimeTs` | string |  |
| `createtimeUtc` | string |  |
| `customertype` | string |  |
| `email` | string |  |
| `fax` | string |  |
| `fbprofileid` | string |  |
| `firstname` | string |  |
| `homephone` | string |  |
| `href` | string |  |
| `id` | string |  |
| `isblacklisted` | string |  |
| `lastactiontime` | string |  |
| `lastcontacttime` | string |  |
| `lastname` | string |  |
| `locationid` | string |  |
| `modifiedtime` | string |  |
| `modifiedtimeTs` | string |  |
| `modifiedtimeUtc` | string |  |
| `notes` | string |  |
| `officephone` | string |  |
| `oktotext` | string |  |
| `organization` | string |  |
| `qboid` | string |  |
| `qboname` | string |  |
| `qbosendinvoice` | string |  |
| `qbosynctoken` | string |  |
| `qboupdatetime` | string |  |
| `referral` | string |  |
| `repeatcustomer` | string |  |
| `score` | string |  |
| `state` | string |  |
| `street` | string |  |
| `taxexemptid` | string |  |
| `title` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /customers` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

