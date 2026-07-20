# Recommand: List Company Identifiers

Retrieves company identifier records from Recommand.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-identifiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-identifiers?connectionId=$CONNECTION_ID&limit=25&offset=0&companyid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-company-identifiers?${params}`, {
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
| `companyid` | string | yes | companyId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "identifiers": [
        {
          "companyId": "string",
          "createdAt": "string",
          "id": "string",
          "identifier": "string",
          "scheme": "string",
          "updatedAt": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identifiers` | array<object> |  |
| `identifiers[].companyId` | string |  |
| `identifiers[].createdAt` | string |  |
| `identifiers[].id` | string |  |
| `identifiers[].identifier` | string |  |
| `identifiers[].scheme` | string |  |
| `identifiers[].updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/companies/:companyId/identifiers` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-company-identifiers.md) for the provider-specific parameters and requirements.

