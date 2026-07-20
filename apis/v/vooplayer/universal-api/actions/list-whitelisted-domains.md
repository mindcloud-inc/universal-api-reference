# Vooplayer: List Whitelisted Domains

Retrieves whitelisted domains from your Vooplayer account.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-whitelisted-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-whitelisted-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-whitelisted-domains?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Whitelisted domain. |

## Native endpoint

Through the native Vooplayer API, this operation is `GET /api/user/domain` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whitelisted-domains.md) for the provider-specific parameters and requirements.

