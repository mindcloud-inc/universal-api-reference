# Five9: Campaign Settings



```
GET https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Five9 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings?connectionId=$CONNECTION_ID&domainID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/five9/latest/actions/campaign-settings?${params}`, {
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
| `domainID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Five9 API returns.

## Native endpoint

Through the native Five9 API, this operation is `GET https://api.prod.us.five9.net/acl/v1/domains/:domainID/permissions/campaignmgmt.ani-settings.view` (base URL `https://api.prod.us.five9.net/acl/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/campaign-settings.md) for the provider-specific parameters and requirements.

