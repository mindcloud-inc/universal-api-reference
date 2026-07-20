# Mews: Get Configuration

Retrieves enterprise configuration from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-configuration?${params}`, {
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
      "enterprise": {},
      "isIdentityDocumentNumberRequired": true,
      "nowUtc": "2026-05-07T12:00:00.000Z",
      "paymentCardStorage": {},
      "service": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enterprise` | object | Enterprise configuration payload. |
| `isIdentityDocumentNumberRequired` | boolean | Whether identity document numbers are required. |
| `nowUtc` | date | Current server time in UTC. |
| `paymentCardStorage` | object | Payment card storage settings. |
| `service` | object | Service configuration payload when present. |

## Native endpoint

Through the native Mews API, this operation is `POST /configuration/get` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-configuration.md) for the provider-specific parameters and requirements.

