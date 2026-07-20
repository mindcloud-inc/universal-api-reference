# OneDesk: Update Customer By External ID

Updates a customer in OneDesk by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/update-customer-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/update-customer-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/update-customer-by-external-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | External ID of the customer to update. |
| `lastName` | string | no | Updated last name for the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Update result code. |

## Native endpoint

Through the native OneDesk API, this operation is `POST /rest/public/customers/externalId/:externalId` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-by-external-id.md) for the provider-specific parameters and requirements.

