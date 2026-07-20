# Kylas CRM: Check Lead Duplicates



```
GET https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kylas CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kylasCRM/latest/actions/check-lead-duplicates?${params}`, {
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
      "hasDuplicate": true,
      "message": "string",
      "metaData": {},
      "records": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasDuplicate` | boolean | Whether the lead has duplicates. |
| `message` | string | Optional message from Kylas about duplicate evaluation. |
| `metaData` | object | Additional metadata for duplicate records. |
| `records` | object | Duplicate lead records payload, when duplicates are present. |

## Native endpoint

Through the native Kylas CRM API, this operation is `GET /leads/{leadId}/has-duplicates` (base URL `https://api.kylas.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-lead-duplicates.md) for the provider-specific parameters and requirements.

