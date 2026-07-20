# Raklet: Delete Contact Address



```
DELETE https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raklet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-address?connectionId=$CONNECTION_ID&organisationMembershipId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organisationMembershipId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raklet/latest/actions/delete-contact-address?${params}`, {
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
| `organisationMembershipId` | string | yes | Raklet contact membership identifier for the address owner. |
| `id` | string | yes | Raklet address identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "city": "string",
        "country": "string",
        "county": "string",
        "details": "string",
        "fullAddress": "string",
        "id": "string",
        "postalCode": "string",
        "state": "string"
      },
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
| `data.city` | string | Address city. |
| `data.country` | string | Address country. |
| `data.county` | string | County value returned by Raklet. |
| `data.details` | string | Deleted address line details. |
| `data.fullAddress` | string | Deleted full address string. |
| `data.id` | string | Deleted Raklet address identifier. |
| `data.postalCode` | string | Postal code returned by Raklet. |
| `data.state` | string | Address state. |
| `errors` | array<object> | Raklet error collection. |
| `isSuccess` | boolean | Whether Raklet marked the request successful. |

## Native endpoint

Through the native Raklet API, this operation is `DELETE /organisations/:organisationId/contacts/:organisationMembershipId/addresses/:id` (base URL `https://api.raklet.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-address.md) for the provider-specific parameters and requirements.

