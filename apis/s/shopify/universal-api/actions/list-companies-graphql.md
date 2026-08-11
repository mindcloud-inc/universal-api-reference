# Shopify: List Companies

Retrieves companies from Shopify with GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-companies-graphql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-companies-graphql?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-companies-graphql?${params}`, {
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
| `companyQuery` | string | no | Optional Shopify company search query string. Leave blank to list companies. Example: `name:Acme`. |
| `externalId` | string | no | Find the Shopify B2B company whose externalId matches this external source-system ID. Example: `External company ID`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAfter` | string | no | Optional lower bound for Shopify created_at company search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `createdBefore` | string | no | Optional upper bound for Shopify created_at company search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `updatedAfter` | string | no | Optional lower bound for Shopify updated_at company search, for example 2026-03-01 or 2026-03-01T00:00:00Z. Example: `2026-03-01`. |
| `updatedBefore` | string | no | Optional upper bound for Shopify updated_at company search, for example 2026-04-01 or 2026-04-01T00:00:00Z. Example: `2026-04-01`. |
| `afterCursor` | string | no | Optional cursor for manually continuing from a previous page. Standard pagination controls handle this automatically in most workflows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": {
        "nodes": [
          {
            "customer": {
              "email": "ava@example.com",
              "firstName": "Ava",
              "id": "string",
              "lastName": "Chen"
            },
            "id": "string"
          }
        ]
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "locations": {
        "nodes": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts.nodes[].customer.email` | string |  |
| `contacts.nodes[].customer.firstName` | string |  |
| `contacts.nodes[].customer.id` | string | Associated Shopify Customer GID |
| `contacts.nodes[].customer.lastName` | string |  |
| `contacts.nodes[].id` | string | Shopify Company Contact GID |
| `createdAt` | date | Company creation time |
| `externalId` | string | External source-system company ID |
| `id` | string | Shopify Company GID |
| `locations.nodes[].id` | string | Shopify Company Location GID |
| `locations.nodes[].name` | string | Company location name |
| `name` | string | Shopify company name |
| `updatedAt` | date | Company last update time |

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies-graphql.md) for the provider-specific parameters and requirements.

