# Fingertip: Update Site



```
PUT https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessType` | string | no | Type of business the site represents, can be null |
| `description` | string | no | Description of the site, can be null |
| `homePageId` | string | no | ID of the site's home page, can be null |
| `locationId` | string | no | ID of the associated location, can be null |
| `name` | string | no | Name of the site |
| `siteId` | string | yes | ID of the site to update |
| `slug` | string | no | URL-friendly identifier for the site |
| `status` | string | no | Current status of the site |
| `timeZone` | string | no | Time zone for the site, can be null |
| `workspaceId` | string | no | ID of the workspace this site belongs to, can be null |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fingertip API returns.

## Native endpoint

Through the native Fingertip API, this operation is `PATCH /v1/sites/:siteId` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site.md) for the provider-specific parameters and requirements.

