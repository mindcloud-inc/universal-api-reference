# Superglue: Get Tool Details

Retrieves tool details from Superglue.

```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-tool-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-tool-details?connectionId=$CONNECTION_ID&toolId=stock-email-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "toolId": "stock-email-alert"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/get-tool-details?${params}`, {
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
| `toolId` | string | yes | ID of the Superglue tool. Example: `stock-email-alert`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "inputSchema": {},
      "instruction": "string",
      "outputTransform": "string",
      "steps": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Tool creation timestamp. |
| `id` | string | Superglue tool identifier. |
| `inputSchema` | object | JSON schema for tool inputs. |
| `instruction` | string | Human-readable instruction describing what the tool does. |
| `outputTransform` | string | Optional output transformation expression. |
| `steps` | array<object> | Ordered execution steps that make up the tool. |
| `updatedAt` | date | Tool update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `GET /tools/:toolId` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tool-details.md) for the provider-specific parameters and requirements.

