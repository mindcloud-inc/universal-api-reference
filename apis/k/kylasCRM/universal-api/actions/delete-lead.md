# Kylas CRM: Delete Lead

Deletes an existing lead from Kylas CRM.

```
DELETE https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/delete-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/delete-lead?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/delete-lead?${params}`, {
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
| `leadId` | string | no | The Kylas lead ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseBody": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseBody` | string | Kylas returns an empty response body on successful lead deletion. |

## Native endpoint

Through the native Kylas CRM API, this operation is `DELETE /leads/{leadId}` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lead.md) for the provider-specific parameters and requirements.

