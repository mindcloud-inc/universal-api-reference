# Bigin by Zoho CRM: Run COQL Query

Runs a COQL query in Bigin by Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/run-coql-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bigin by Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/run-coql-query?connectionId=$CONNECTION_ID&selectQuery=select%20id%2C%20Last_Name%20from%20Contacts%20where%20Last_Name%20is%20not%20null%20limit%2010" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "selectQuery": "select id, Last_Name from Contacts where Last_Name is not null limit 10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/run-coql-query?${params}`, {
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
| `selectQuery` | string | yes | The COQL query string to execute. Example: `select id, Last_Name from Contacts where Last_Name is not null limit 10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bigin by Zoho CRM API returns.

## Native endpoint

Through the native Bigin by Zoho CRM API, this operation is `POST /coql` (base URL `{{credentials.accessTokenRequest.api_domain}}/bigin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-coql-query.md) for the provider-specific parameters and requirements.

