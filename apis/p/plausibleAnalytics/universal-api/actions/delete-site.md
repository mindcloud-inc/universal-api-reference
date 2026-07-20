# Plausible Analytics: Delete Site

Deletes an existing site from Plausible Analytics.

```
DELETE https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/delete-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/delete-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/delete-site?${params}`, {
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
      "deleted": true,
      "domain": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `domain` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `DELETE /api/v1/sites/:domain` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-site.md) for the provider-specific parameters and requirements.

