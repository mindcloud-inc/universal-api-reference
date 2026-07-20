# Clicksign: Delete Requirement

Deletes an existing requirement from Clicksign.

```
DELETE https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/delete-requirement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/delete-requirement?connectionId=$CONNECTION_ID&envelopeId=string&requirementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string",
  "requirementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/delete-requirement?${params}`, {
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
| `envelopeId` | string | yes | The UUID of the envelope. |
| `requirementId` | string | yes | The UUID of the requirement. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `DELETE /envelopes/:envelope_id/requirements/:requirement_id` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-requirement.md) for the provider-specific parameters and requirements.

