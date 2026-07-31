# wtfismyip: Get Runner IP Information as YAML



```
GET https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information-as-yaml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a wtfismyip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information-as-yaml?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-information-as-yaml?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native wtfismyip API returns.

## Native endpoint

Through the native wtfismyip API, this operation is `GET /yaml` (base URL `https://wtfismyip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-runner-ip-information-as-yaml.md) for the provider-specific parameters and requirements.

