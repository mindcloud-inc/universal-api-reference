# Raklet: Set Primary Contact Address



```
PUT https://connect.mindcloud.co/v1/universal/raklet/latest/actions/set-primary-contact-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/set-primary-contact-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationMembershipId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raklet/latest/actions/set-primary-contact-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationMembershipId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationMembershipId` | string | yes | Raklet contact membership identifier for the address owner. |
| `id` | string | yes | Raklet address identifier to promote as primary. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "errors": [
        {}
      ],
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Raklet response code. |
| `errors` | array<object> | Raklet error collection. |
| `isSuccess` | boolean | Whether Raklet marked the request successful. |

## Native endpoint

Through the native Raklet API, this operation is `PATCH /organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id/SetPrimary` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-primary-contact-address.md) for the provider-specific parameters and requirements.

