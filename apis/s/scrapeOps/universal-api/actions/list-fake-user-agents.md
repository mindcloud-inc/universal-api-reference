# ScrapeOps: List Fake User Agents

Retrieves fake user agents from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-fake-user-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-fake-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-fake-user-agents?${params}`, {
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
| `numResults` | number | no | How many fake user agents to return. |
| `mobile` | boolean | no | Return mobile user agents only when true. |

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
| `value` | string | The fake user agent string returned by ScrapeOps. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET http://headers.scrapeops.io/v1/user-agents` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fake-user-agents.md) for the provider-specific parameters and requirements.

