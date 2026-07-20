# Zoho CRM: Get Records through COQL Query

Retrieves records from Zoho CRM using a COQL query.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-records-through-coql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-records-through-coql-query?connectionId=$CONNECTION_ID&selectQuery=select%20id%2C%20last_name%2C%20first_name%2C%20email%20from%20Users%20where%20id%20is%20not%20null%20limit%205" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "selectQuery": "select id, last_name, first_name, email from Users where id is not null limit 5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-records-through-coql-query?${params}`, {
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
| `selectQuery` | string | yes | Single read-only COQL SELECT query. Use one SELECT statement only. Example: `select id, last_name, first_name, email from Users where id is not null limit 5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho CRM API returns.

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /coql` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-records-through-coql-query.md) for the provider-specific parameters and requirements.

