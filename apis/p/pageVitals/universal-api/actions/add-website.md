# PageVitals: Add Website



```
POST https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain of the website, without https:// and paths. |
| `displayName` | string | no | Optional displayed name for the website in the admin UI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "domain": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `domain` | string |  |
| `id` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `POST /account/websites` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-website.md) for the provider-specific parameters and requirements.

