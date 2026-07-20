# Process Street: List Form Field Options



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-form-field-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-form-field-options?connectionId=$CONNECTION_ID&workflowId=string&formFieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string",
  "formFieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/list-form-field-options?${params}`, {
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
| `workflowId` | string | yes | The ID of the workflow. |
| `formFieldId` | string | yes | The ID of the form field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflows/:workflowId/form-fields/:formFieldId/options` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-field-options.md) for the provider-specific parameters and requirements.

