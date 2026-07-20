# Aqara Home for US: Delete Position

Deletes an existing position from Aqara Home for US.

```
DELETE https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/delete-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for US `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/delete-position?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/delete-position?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aqara Home for US API returns.

## Native endpoint

Through the native Aqara Home for US API, this operation is `POST /` (base URL `https://open-usa.aqara.com/v3.0/open/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-position.md) for the provider-specific parameters and requirements.

