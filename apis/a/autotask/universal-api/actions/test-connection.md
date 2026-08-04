# Autotask: Test Connection



```
GET https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autotask/latest/actions/test-connection?${params}`, {
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
      "build": "string",
      "customerType": "string",
      "majorVersion": "string",
      "minorVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `build` | string | Autotask build number. |
| `customerType` | string | Autotask customer type. |
| `majorVersion` | string | Autotask major version. |
| `minorVersion` | string | Autotask minor version. |

## Native endpoint

Through the native Autotask API, this operation is `GET /Version` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-connection.md) for the provider-specific parameters and requirements.

