# Deepgram: List Project Billing Fields

Retrieves project billing fields from Deepgram.

```
GET https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-billing-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-billing-fields?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/list-project-billing-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Deepgram project identifier. |
| `start` | string | no | Start date for the requested billing-field range in YYYY-MM-DD format. |
| `end` | string | no | End date for the requested billing-field range in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessors": [
        "string"
      ],
      "deployments": [
        "string"
      ],
      "lineItems": {},
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessors` | array<string> |  |
| `deployments` | array<string> |  |
| `lineItems` | object |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Deepgram API, this operation is `GET /v1/projects/:project_id/billing/fields` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-billing-fields.md) for the provider-specific parameters and requirements.

