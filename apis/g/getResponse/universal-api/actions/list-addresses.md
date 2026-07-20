# GetResponse: List Addresses

Retrieves a list of addresses from GetResponse.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-addresses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-addresses?${params}`, {
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
| `name` | string | no | Filter addresses by name |
| `firstName` | string | no | Filter addresses by first name |
| `lastName` | string | no | Filter addresses by last name |
| `address1` | string | no | Filter by address line 1 |
| `address2` | string | no | Filter by address line 2 |
| `city` | string | no | Filter addresses by city |
| `zip` | string | no | Filter addresses by ZIP code |
| `province` | string | no | Filter addresses by province |
| `provinceCode` | string | no | Filter addresses by province code |
| `phone` | string | no | Filter addresses by phone |
| `company` | string | no | Filter addresses by company |
| `createdOnFrom` | string | no | Return addresses created on or after this date |
| `createdOnTo` | string | no | Return addresses created on or before this date |
| `sortCreatedOn` | string | no | Sort addresses by creation date |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressId": "string",
      "countryCode": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressId` | string |  |
| `countryCode` | string |  |
| `name` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /addresses` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

