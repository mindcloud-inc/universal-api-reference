# Bookvault: Delete Address

Deletes an existing address from Bookvault.

```
DELETE https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/delete-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/delete-address?connectionId=$CONNECTION_ID&commonAddrId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commonAddrId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/delete-address?${params}`, {
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
| `commonAddrId` | number | yes | Bookvault common address ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address1": "string",
      "Addressee": "string",
      "CommonAddrID": 1,
      "Company": "string",
      "Country": {},
      "Email": "ava@example.com",
      "Postcode": "string",
      "Town": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address1` | string |  |
| `Addressee` | string |  |
| `CommonAddrID` | number |  |
| `Company` | string |  |
| `Country` | object |  |
| `Email` | string |  |
| `Postcode` | string |  |
| `Town` | string |  |

## Native endpoint

Through the native Bookvault API, this operation is `DELETE /Addresses` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-address.md) for the provider-specific parameters and requirements.

