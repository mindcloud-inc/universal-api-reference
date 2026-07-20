# Agicap: List Organization Entities

Retrieves organization entities for an Agicap organization.

```
GET https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-organization-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agicap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-organization-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agicap/latest/actions/list-organization-entities?${params}`, {
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
| `pageNumber` | number | no | Page number to retrieve. Agicap pages start at 1. Default: `1`. Example: `1`. |
| `pageSize` | number | no | Number of entities to return per page. Default: `100`. Example: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Entity country code or label when returned by Agicap. |
| `id` | number | Agicap entity identifier from OrganizationEntityPresentation. |
| `name` | string | Agicap entity name. |

## Native endpoint

Through the native Agicap API, this operation is `GET /public/organizations/v1/:organizationId/entities` (base URL `https://api.agicap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-entities.md) for the provider-specific parameters and requirements.

