# Agendor: List Organizations

Finds organizations in Agendor by search filters.

```
GET https://connect.mindcloud.co/v1/universal/agendor/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agendor/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agendor/latest/actions/list-organizations?${params}`, {
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
| `cnpj` | string | no | CNPJ prefix to search for. |
| `email` | string | no | Contact email prefix to search for. |
| `name` | string | no | Organization name prefix to search for. |
| `page` | number | no | Page of results to fetch. |
| `per_page` | number | no | Number of results to return per page (max 100). |
| `updatedAtGt` | date | no | Only include organizations updated after this ISO-8601 timestamp. |
| `updatedAtLt` | date | no | Only include organizations updated before this ISO-8601 timestamp. |
| `withCustomFields` | boolean | no | Include custom fields in the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agendor API returns.

## Native endpoint

Through the native Agendor API, this operation is `GET /organizations` (base URL `https://api.agendor.com.br/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

