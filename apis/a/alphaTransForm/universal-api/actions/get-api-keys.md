# Alpha TransForm: Get API Keys

Retrieves API keys from Alpha TransForm.

```
GET https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alpha TransForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-api-keys?${params}`, {
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
      "apikey": "string",
      "dateGranted": "string",
      "dateRevoked": "string",
      "revoked": "string",
      "scopes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apikey` | string |  |
| `dateGranted` | string |  |
| `dateRevoked` | string |  |
| `revoked` | string |  |
| `scopes` | string |  |

## Native endpoint

Through the native Alpha TransForm API, this operation is `GET /GetAPIKeys` (base URL `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-keys.md) for the provider-specific parameters and requirements.

