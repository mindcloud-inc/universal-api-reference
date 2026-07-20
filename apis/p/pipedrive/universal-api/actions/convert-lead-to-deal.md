# Pipedrive: Convert Lead To Deal

Converts a lead to a deal in Pipedrive.

```
POST https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-lead-to-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-lead-to-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/convert-lead-to-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lead ID to convert into a deal. |
| `stageId` | number | no | Optional stage ID where the created deal will be placed. |
| `pipelineId` | number | no | Optional pipeline ID where the created deal will be placed. |

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

Through the native Pipedrive API, this operation is `POST v2/leads/:id/convert/deal` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-lead-to-deal.md) for the provider-specific parameters and requirements.

