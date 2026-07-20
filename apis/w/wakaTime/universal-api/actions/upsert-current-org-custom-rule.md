# WakaTime: Upsert Current Org Custom Rule

Updates custom rules for a WakaTime organization.

```
PUT https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/upsert-current-org-custom-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WakaTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/upsert-current-org-custom-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/upsert-current-org-custom-rule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native WakaTime API, this operation is `PUT /users/current/orgs/:org/custom_rules` (base URL `https://api.wakatime.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-current-org-custom-rule.md) for the provider-specific parameters and requirements.

