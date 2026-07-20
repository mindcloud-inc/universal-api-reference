# Airslate: Add Template Tag

Adds a tag to a template in airSlate.

```
POST https://connect.mindcloud.co/v1/universal/airslate/latest/actions/add-template-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airslate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airslate/latest/actions/add-template-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airslate/latest/actions/add-template-tag', {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Airslate API, this operation is `POST /organizations/{organization_id}/templates/{template_id}/tags` (base URL `https://api.airslate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-template-tag.md) for the provider-specific parameters and requirements.

