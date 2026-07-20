# SWELLEnterprise: Get Portal Configuration

Retrieves portal configuration from SWELLEnterprise.

```
GET https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-configuration?${params}`, {
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
      "data": {
        "allowFileSharing": true,
        "enabledModules": [
          "string"
        ],
        "isActive": true,
        "portalLogo": {},
        "portalName": "Ava Chen",
        "primaryColor": "string",
        "secondaryColor": "string",
        "showActivityFeed": true,
        "tokenExpirationDays": 1,
        "welcomeMessage": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.allowFileSharing` | boolean |  |
| `data.enabledModules[]` | string |  |
| `data.isActive` | boolean |  |
| `data.portalLogo` | object |  |
| `data.portalName` | string |  |
| `data.primaryColor` | string |  |
| `data.secondaryColor` | string |  |
| `data.showActivityFeed` | boolean |  |
| `data.tokenExpirationDays` | number |  |
| `data.welcomeMessage` | object |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `GET /client-portal/config` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-configuration.md) for the provider-specific parameters and requirements.

