# Pipedrive: Convert Deal To Lead

Converts a deal to a lead in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-deal-to-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-deal-to-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-deal-to-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique ID of the deal to convert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionId` | string |  |

## Native endpoint

Through the native Pipedrive API, this operation is `POST v2/deals/:id/convert/lead` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-deal-to-lead.md) for the provider-specific parameters and requirements.

