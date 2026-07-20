# RoboAuditor: Get Lead Token



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-token?connectionId=$CONNECTION_ID&domainId=1&token=string&websiteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1",
  "token": "string",
  "websiteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/get-lead-token?${params}`, {
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
| `domainId` | number | yes | Domain identifier (numeric). |
| `token` | string | yes | Report token value. |
| `websiteUrl` | string | yes | Website URL associated with the lead/report token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Resolved lead token returned by the provider. |

## Native endpoint

Through the native RoboAuditor API, this operation is `POST /lead/getToken` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-token.md) for the provider-specific parameters and requirements.

