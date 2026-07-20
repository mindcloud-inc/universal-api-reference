# Marketing Master IO: Enable Facebook Page

Enables an imported Facebook page in Marketing Master IO.

```
PUT https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/enable-facebook-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/enable-facebook-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "page_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/enable-facebook-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "page_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | boolean |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `POST /v1/facebook_pages/:page_id` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-facebook-page.md) for the provider-specific parameters and requirements.

