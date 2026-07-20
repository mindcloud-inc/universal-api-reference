# GMass: List Unsubscribed Domains

Retrieves unsubscribed domains from your GMass account.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-unsubscribed-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-unsubscribed-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-unsubscribed-domains?${params}`, {
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
      "unsubscribeTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Domain on the account unsubscribe domain list. |
| `unsubscribeTime` | date | Time the domain was unsubscribed. |

## Native endpoint

Through the native GMass API, this operation is `GET /unsubscribes/domains` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unsubscribed-domains.md) for the provider-specific parameters and requirements.

