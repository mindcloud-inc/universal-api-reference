# OKSign: Retrieve Audit Trail

Retrieves an audit trail report from OKSign.

```
GET https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-audit-trail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OKSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-audit-trail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-audit-trail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OKSign API returns.

## Native endpoint

Through the native OKSign API, this operation is `GET /audittrail/retrieve` (base URL `https://www.oksign.be/services/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-audit-trail.md) for the provider-specific parameters and requirements.

