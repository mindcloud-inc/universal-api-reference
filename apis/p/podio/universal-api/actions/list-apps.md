# Podio: List Apps

Retrieves a list of apps from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-apps?${params}`, {
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
| `text` | string | no | Search term matching app names, item names, or workspace names. Example: `sales pipeline`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | The maximum number of apps to return. Example: `4`. |
| `order` | string | no | The order to return the apps in. Example: `score`. |
| `excludeDemo` | boolean | no | True if apps from the demo workspace should be excluded. |
| `excludeAppIds` | string | no | Comma-separated list of app IDs to exclude from the returned list. Accepts multiple values in one string, delimited by `,`. Example: `12345,67890`. |
| `referenceableInOrg` | number | no | Organization ID to filter apps by. Example: `123456`. |
| `right` | string | no | The right the user must have on the returned apps. |
| `targetSpaceId` | number | no | Preferred space ID to prioritize apps from. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": 1,
      "config": {},
      "currentRevision": 1,
      "defaultViewId": 1,
      "isDefault": true,
      "itemAccountingInfo": {},
      "link": "https://example.com",
      "linkAdd": "https://example.com",
      "sharefileVaultUrl": "https://example.com",
      "spaceId": 1,
      "status": "string",
      "url": "https://example.com",
      "urlAdd": "https://example.com",
      "urlLabel": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | number |  |
| `config` | object |  |
| `currentRevision` | number |  |
| `defaultViewId` | number |  |
| `isDefault` | boolean |  |
| `itemAccountingInfo` | object |  |
| `link` | string |  |
| `linkAdd` | string |  |
| `sharefileVaultUrl` | string |  |
| `spaceId` | number |  |
| `status` | string |  |
| `url` | string |  |
| `urlAdd` | string |  |
| `urlLabel` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /app/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps.md) for the provider-specific parameters and requirements.

