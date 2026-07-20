# Coralogix: List Outgoing Webhooks



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-outgoing-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-outgoing-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-outgoing-webhooks?${params}`, {
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
      "deployed": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployed` | array<object> | deployed returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /integrations/webhooks/v1` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-outgoing-webhooks.md) for the provider-specific parameters and requirements.

