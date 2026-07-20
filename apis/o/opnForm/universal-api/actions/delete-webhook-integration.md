# OpnForm: Delete Webhook Integration

Deletes an existing webhook integration from OpnForm.

```
DELETE https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/delete-webhook-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/delete-webhook-integration?connectionId=$CONNECTION_ID&formId=1&integrationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1",
  "integrationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/delete-webhook-integration?${params}`, {
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
| `formId` | number | yes |  |
| `integrationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OpnForm API, this operation is `DELETE /open/forms/:formId/integrations/:integrationId` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-integration.md) for the provider-specific parameters and requirements.

