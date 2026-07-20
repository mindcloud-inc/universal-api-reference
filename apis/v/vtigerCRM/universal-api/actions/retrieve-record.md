# Vtiger CRM: Retrieve Record

Retrieves a record from Vtiger CRM.

```
GET https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/retrieve-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/retrieve-record?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/retrieve-record?${params}`, {
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
| `id` | string | yes | Vtiger record id such as 4x489. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger record id. |
| `label` | string | Human-readable record label. |
| `url` | string | Vtiger record URL. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `GET /retrieve` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-record.md) for the provider-specific parameters and requirements.

