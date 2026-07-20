# Virtually: List Custom Data Records

Retrieves custom data records from Virtually.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-custom-data-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-custom-data-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-custom-data-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId/customData` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-data-records.md) for the provider-specific parameters and requirements.

