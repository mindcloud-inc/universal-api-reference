# InflatableOffice: Create Customer

Creates a new customer in InflatableOffice.

```
POST https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-customer', {
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
| `cellphone` | string | no |  |
| `city` | string | no |  |
| `cleartags` | string | no |  |
| `country` | string | no |  |
| `customertype` | string | no |  |
| `customfields_ids` | string | no |  |
| `custtags` | string | no |  |
| `email` | string | no |  |
| `fax` | string | no |  |
| `firstname` | string | no |  |
| `homephone` | string | no |  |
| `lastname` | string | no |  |
| `name` | string | no |  |
| `notes` | string | no |  |
| `officephone` | string | no |  |
| `organization` | string | no |  |
| `state` | string | no |  |
| `street` | string | no |  |
| `zip` | string | no |  |

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
| `recordid` | string | Created customer ID. |
| `requestTime` | number | Provider request timestamp. |
| `status` | number | HTTP status code returned by InflatableOffice. |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /customers` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

