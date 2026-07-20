# Pledge: List Organizations

Retrieves organizations from Pledge.

```
GET https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-organizations?${params}`, {
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
| `q` | string | no | Keyword search on name, alias, or mission. |
| `ngoId` | string | no | Filter by NGO ID. |
| `causeId` | number | no | Filter by cause ID. |
| `country` | string | no | Filter by ISO 3166-1 alpha-2 country code. |
| `region` | string | no | Filter by region. |
| `postalCode` | string | no | Filter by postal or zip code. |
| `lat` | string | no | Latitude for proximity search. Must be paired with longitude. |
| `lon` | string | no | Longitude for proximity search. Must be paired with latitude. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "city": "string",
      "country": "string",
      "disbursementType": "string",
      "id": "string",
      "lat": {},
      "logoUrl": "https://example.com",
      "lon": {},
      "mission": {},
      "name": "Ava Chen",
      "ngoId": "string",
      "postalCode": "string",
      "profileUrl": "https://example.com",
      "region": "string",
      "street1": "string",
      "street2": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `city` | string |  |
| `country` | string |  |
| `disbursementType` | string |  |
| `id` | string |  |
| `lat` | object |  |
| `logoUrl` | string |  |
| `lon` | object |  |
| `mission` | object |  |
| `name` | string |  |
| `ngoId` | string |  |
| `postalCode` | string |  |
| `profileUrl` | string |  |
| `region` | string |  |
| `street1` | string |  |
| `street2` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `GET /organizations` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

