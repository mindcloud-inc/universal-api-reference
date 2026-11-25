# Epicor Prophet 21: Query OData View with Body



```
GET https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-view-with-body
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Epicor Prophet 21 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-view-with-body?connectionId=$CONNECTION_ID&viewName=p21_view_supplier&queryOptions=%24select%3Dsupplier_id%2Csupplier_name%26%24top%3D25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "p21_view_supplier",
  "queryOptions": "$select=supplier_id,supplier_name&$top=25"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/epicorProphet21/latest/actions/query-odata-view-with-body?${params}`, {
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
| `viewName` | list<string> | yes | Example: `p21_view_supplier`. |
| `queryOptions` | string | yes | Example: `$select=supplier_id,supplier_name&$top=25`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Epicor Prophet 21 API returns.

## Native endpoint

Through the native Epicor Prophet 21 API, this operation is `POST /odataservice/odata/view/:viewName/$query` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-odata-view-with-body.md) for the provider-specific parameters and requirements.

