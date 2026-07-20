# OneDesk: Search Customer Organizations

Finds customer organizations in OneDesk by filters.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customer-organizations?${params}`, {
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
| `properties[]` | array<object> | no | Array of OneDesk property filters. |
| `properties[].operation` | string | no | Comparison operation to apply to the property. |
| `properties[].property` | string | no | Name of property to be filtered. |
| `properties[].value` | string | no | Value used in the filter comparison. |
| `limit` | number | no | Maximum number of customer organizations to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneDesk API returns.

## Native endpoint

Through the native OneDesk API, this operation is `POST /rest/public/customer-organizations/filter` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-customer-organizations.md) for the provider-specific parameters and requirements.

