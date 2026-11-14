# Infor ReserveCloud SCS: List Transaction



```
GET https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infor ReserveCloud SCS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-transaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inforSCS/latest/actions/list-transaction?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Infor ReserveCloud SCS API returns.

## Native endpoint

Through the native Infor ReserveCloud SCS API, this operation is `GET https://www.reservecloud.com/gateway/request`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction.md) for the provider-specific parameters and requirements.

