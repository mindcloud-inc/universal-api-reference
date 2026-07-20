# ONLYOFFICE DocSpace: Get Portal Capabilities

Retrieves portal capabilities from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-capabilities?${params}`, {
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
      "identityServerEnabled": true,
      "ldapEnabled": true,
      "oauthEnabled": true,
      "providers": [
        "string"
      ],
      "ssoLabel": "string",
      "ssoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `identityServerEnabled` | boolean |  |
| `ldapEnabled` | boolean |  |
| `oauthEnabled` | boolean |  |
| `providers[]` | string |  |
| `ssoLabel` | string |  |
| `ssoUrl` | string |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/capabilities` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-capabilities.md) for the provider-specific parameters and requirements.

