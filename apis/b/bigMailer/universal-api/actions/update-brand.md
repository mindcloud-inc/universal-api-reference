# BigMailer: Update Brand

Updates an existing brand in BigMailer.

```
PUT https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigMailer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "brandId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigMailer/latest/actions/update-brand', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "brandId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `brandId` | string | yes | ID of the brand to update. |
| `name` | string | no | Name of the brand. |
| `fromName` | string | no | Default sender name for the brand. |
| `fromEmail` | string | no | Default sender email for the brand. |
| `bounceDangerPercent` | number | no | Bounce percentage that pauses bulk campaigns automatically. |
| `maxSoftBounces` | number | no | Maximum number of soft bounces before a contact is treated as undeliverable. |
| `url` | string | no | Website URL associated with the brand. |
| `unsubscribeText` | string | no | Message displayed on the brand unsubscribe page. |
| `contactLimit` | number | no | Maximum number of contacts allowed in the brand. |
| `logo` | string | no | Base64 encoded brand logo image. |
| `connectionId` | string | no | ID of the sending connection used by the brand. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigMailer API returns.

## Native endpoint

Through the native BigMailer API, this operation is `POST /brands/:brand_id` (base URL `https://api.bigmailer.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand.md) for the provider-specific parameters and requirements.

