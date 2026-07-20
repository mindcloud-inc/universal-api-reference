# Coralogix: Get Policy Priority Settings



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-policy-priority-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-policy-priority-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-policy-priority-settings?${params}`, {
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
      "logsPolicySettings": {},
      "spansPolicySettings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logsPolicySettings` | object | logsPolicySettings returned by Coralogix. |
| `spansPolicySettings` | object | spansPolicySettings returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /dataplans/policies/v1/getPolicyPrioritySettings` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-policy-priority-settings.md) for the provider-specific parameters and requirements.

