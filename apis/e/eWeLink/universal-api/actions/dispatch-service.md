# eWeLink: Dispatch Service

Retrieves dispatch service information from eWeLink.

```
GET https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/dispatch-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/dispatch-service?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/dispatch-service?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "error": 1,
      "IP": "string",
      "port": 1,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `error` | number |  |
| `IP` | string |  |
| `port` | number |  |
| `reason` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `GET https://{{credentials.authorizeRequest.region}}-dispa.coolkit.cc/dispatch/app` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dispatch-service.md) for the provider-specific parameters and requirements.

