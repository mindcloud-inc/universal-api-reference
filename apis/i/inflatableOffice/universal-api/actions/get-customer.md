# InflatableOffice: Get Customer

Retrieves a customer from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cellphone": "string",
      "city": "string",
      "country": "string",
      "createtimeUtc": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "href": "string",
      "id": "string",
      "lastname": "Chen",
      "modifiedtimeUtc": "string",
      "organization": "string",
      "requestTime": 1,
      "state": "string",
      "street": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cellphone` | string | Cell phone number. |
| `city` | string | City. |
| `country` | string | Country. |
| `createtimeUtc` | string | Created timestamp in UTC. |
| `email` | string | Email address. |
| `firstname` | string | Customer first name. |
| `href` | string | API resource URL. |
| `id` | string | Customer ID. |
| `lastname` | string | Customer last name. |
| `modifiedtimeUtc` | string | Modified timestamp in UTC. |
| `organization` | string | Organization name. |
| `requestTime` | number | Provider request timestamp. |
| `state` | string | State or region. |
| `street` | string | Street address. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /customers/:customerId` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

