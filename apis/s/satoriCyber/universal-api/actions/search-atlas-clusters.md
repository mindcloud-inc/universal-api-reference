# Satori Cyber: Search Atlas Clusters

Finds Atlas clusters in Satori Cyber.

```
GET https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-atlas-clusters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satori Cyber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-atlas-clusters?connectionId=$CONNECTION_ID&accountId=94c20cf0-e590-4f8a-becb-510f75be7f8e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "94c20cf0-e590-4f8a-becb-510f75be7f8e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-atlas-clusters?${params}`, {
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
| `accountId` | string | yes | Satori account ID for authorization analytics scope. Example: `94c20cf0-e590-4f8a-becb-510f75be7f8e`. |
| `search` | string | no | Optional search string for atlas cluster matching. Example: `atlas-prod`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `records` | array<object> |  |

## Native endpoint

Through the native Satori Cyber API, this operation is `GET /api/v1/authorization-analytics/search-atlas-clusters` (base URL `https://app.satoricyber.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-atlas-clusters.md) for the provider-specific parameters and requirements.

