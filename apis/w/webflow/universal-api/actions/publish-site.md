# Webflow: Publish Site

Publishes a site in Webflow.

```
PUT https://connect.mindcloud.co/v1/universal/webflow/latest/actions/publish-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/publish-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/publish-site', {
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
| `siteId` | string | yes | Unique identifier of the site. |
| `customDomains[]` | array<string> | no | Optional list of custom domain IDs to publish. |
| `publishToWebflowSubdomain` | boolean | no | Set true to publish to the Webflow subdomain. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customDomains": [
        {}
      ],
      "publishToWebflowSubdomain": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customDomains` | array<object> | Custom domains included in the publish operation. |
| `publishToWebflowSubdomain` | boolean | Whether the site was published to the Webflow subdomain. |

## Native endpoint

Through the native Webflow API, this operation is `POST /sites/:site_id/publish` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-site.md) for the provider-specific parameters and requirements.

