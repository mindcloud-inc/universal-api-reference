# RoboAuditor: Update Domain Settings



```
PUT https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-domain-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-domain-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "whiteLabelUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/update-domain-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "whiteLabelUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whiteLabelUrl` | string | yes | Custom domain URL to bind. |
| `isCnameValid` | boolean | no | Whether DNS CNAME is validated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number | HTTP status code returned by provider (200 on success). |

## Native endpoint

Through the native RoboAuditor API, this operation is `POST /domain-settings/` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain-settings.md) for the provider-specific parameters and requirements.

