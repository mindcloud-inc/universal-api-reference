# Stacker: List Fields

Retrieves fields for a Stacker object.

```
GET https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-fields?connectionId=$CONNECTION_ID&accountId=string&objectSid=string&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "objectSid": "string",
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-fields?${params}`, {
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
| `accountId` | string | yes | Stacker account ID sent as the X-Account-Id header. |
| `objectSid` | string | yes | Object SID from the Stacker endpoint path. |
| `stackId` | string | yes | Stacker stack ID sent as the X-Stack-Id header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_name": "Ava Chen",
      "dropdown_options": [
        {}
      ],
      "label": "string",
      "sid": "string",
      "target_object_sid": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_name` | string | Field API name. |
| `dropdown_options` | array<object> | Dropdown options when the field is a dropdown. |
| `label` | string | Human-readable field label. |
| `sid` | string | Field SID. |
| `target_object_sid` | string | Target object SID for lookup-style fields. |
| `type` | string | Stacker field type. |

## Native endpoint

Through the native Stacker API, this operation is `GET /api/external/objects/:object_sid/fields/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

