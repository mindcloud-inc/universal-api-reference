# MyEmailVerifier: Get Email Analysis Status

Retrieves email analysis service status from MyEmailVerifier.

```
GET https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-email-analysis-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-email-analysis-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-email-analysis-status?${params}`, {
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
      "api_version": "string",
      "service_status": {},
      "status": "string",
      "user_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string | Public API version string. |
| `service_status` | object | Current service capabilities and availability. |
| `status` | string | Whether the status request succeeded. |
| `user_info` | object | Remaining credit and API key summary for the caller. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `GET /email-analysis/status/{{credentials.apiKey}}` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-analysis-status.md) for the provider-specific parameters and requirements.

