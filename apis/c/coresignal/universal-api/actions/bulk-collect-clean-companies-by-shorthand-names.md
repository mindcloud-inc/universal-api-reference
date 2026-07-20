# Coresignal: Bulk Collect Clean Companies By Shorthand Names

Creates a bulk clean company shorthand-name request in Coresignal.

```
POST https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-clean-companies-by-shorthand-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-clean-companies-by-shorthand-names" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-clean-companies-by-shorthand-names', {
  method: 'POST',
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
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `POST /data_requests/company_clean/shorthand_names` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-collect-clean-companies-by-shorthand-names.md) for the provider-specific parameters and requirements.

