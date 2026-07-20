# Anabix CRM: List Contacts

Retrieves contact records from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts?${params}`, {
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
| `data.limit` | number | no | Maximum number of records to return. Anabix documents 200 as the standard maximum. Default: `100`. |
| `data.offset` | number | no | Number of records to skip. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.criteria` | object | no | Filter object keyed by Anabix contact fields, for example email or lastName. |
| `data.includeMetadata` | number | no | Set to 1 to include total record metadata for pagination. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "description": "string",
      "email": "ava@example.com",
      "email2": "ava@example.com",
      "email3": "ava@example.com",
      "firstName": "Ava",
      "gdpr": {},
      "idContact": 1,
      "idOrganization": 1,
      "idOwner": 1,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "organization": "string",
      "phoneNumber": "string",
      "phoneNumber2": "string",
      "phoneNumber3": "string",
      "position": "string",
      "primaryContact": 1,
      "revisionInfo": {},
      "salutation": "string",
      "sex": "string",
      "shippingCity": "string",
      "shippingCode": "string",
      "shippingCountry": "string",
      "shippingStreet": "string",
      "source": "string",
      "title": "Ava Chen",
      "vip": 1,
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `description` | string |  |
| `email` | string |  |
| `email2` | string |  |
| `email3` | string |  |
| `firstName` | string |  |
| `gdpr` | object |  |
| `idContact` | number | Anabix contact ID. |
| `idOrganization` | number | Organization ID when present. |
| `idOwner` | number |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `organization` | string |  |
| `phoneNumber` | string |  |
| `phoneNumber2` | string |  |
| `phoneNumber3` | string |  |
| `position` | string |  |
| `primaryContact` | number |  |
| `revisionInfo` | object |  |
| `salutation` | string |  |
| `sex` | string |  |
| `shippingCity` | string |  |
| `shippingCode` | string |  |
| `shippingCountry` | string |  |
| `shippingStreet` | string |  |
| `source` | string |  |
| `title` | string | Contact display title. |
| `vip` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

