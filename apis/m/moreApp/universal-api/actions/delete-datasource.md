# MoreApp: Delete Datasource

Deletes a datasource from MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-datasource?connectionId=$CONNECTION_ID&customerId=1&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-datasource?${params}`, {
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
| `customerId` | number | yes | MoreApp customer ID. |
| `dataSourceId` | string | yes | Datasource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body on successful datasource deletion; presence indicates the request completed. |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-datasource.md) for the provider-specific parameters and requirements.

