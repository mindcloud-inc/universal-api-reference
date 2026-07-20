# OpenRegister: Search Companies

Finds companies in OpenRegister by name or register details.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-companies?${params}`, {
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
| `query` | string | no | Text search query to find companies by name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `registerNumber` | string | no | Company register number for exact matching. |
| `registerType` | string | no | Type of company register, such as HRB, HRA, PR, GnR, or VR. |
| `registerCourt` | string | no | Court where the company is registered. |
| `active` | boolean | no | Filter for active or inactive companies. |
| `legalForm` | string | no | Legal form of the company, such as gmbh, ag, ug, kg, or ohg. |
| `incorporationDate` | date | no | Date of incorporation in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpenRegister API returns.

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v0/search/company` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

