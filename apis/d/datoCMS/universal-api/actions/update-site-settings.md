# DatoCMS: Update Site Settings



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-site-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-site-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-site-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes` | object | yes | Site settings attributes object. Example: `[object Object]`. |
| `attributes.globalSeo.siteName` | string | no |  |
| `attributes.globalSeo.fallbackSeo` | object | no |  |
| `attributes.globalSeo.fallbackSeo.title` | string | no |  |
| `attributes.globalSeo.fallbackSeo.description` | string | no |  |
| `attributes.globalSeo.fallbackSeo.image` | string | no |  |
| `attributes.globalSeo.fallbackSeo.twitterCard` | string | no |  |
| `attributes.globalSeo.titleSuffix` | string | no |  |
| `attributes.globalSeo.facebookPageUrl` | string | no |  |
| `attributes.globalSeo.twitterAccount` | string | no |  |
| `attributes.locales[]` | array<string> | no |  |
| `attributes.favicon` | string | no |  |
| `attributes.globalSeo` | object | no |  |
| `attributes.name` | string | no |  |
| `attributes.noIndex` | boolean | no |  |
| `attributes.theme` | object | no |  |
| `attributes.forceUseOfSandboxEnvironments` | boolean | no |  |
| `attributes.ipTrackingEnabled` | boolean | no |  |
| `attributes.require2fa` | boolean | no |  |
| `attributes.timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `PUT /site` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site-settings.md) for the provider-specific parameters and requirements.

