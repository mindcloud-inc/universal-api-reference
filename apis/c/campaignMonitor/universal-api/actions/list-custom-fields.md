# Campaign Monitor: List Custom Fields

Retrieves custom fields for a Campaign Monitor list.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-custom-fields?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataType": "string",
      "fieldName": "Ava Chen",
      "fieldOptions": [
        "string"
      ],
      "key": "string",
      "visibleInPreferenceCenter": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType` | string | Campaign Monitor custom field data type. |
| `fieldName` | string | Custom field display name. |
| `fieldOptions` | array<string> | Options configured for the custom field. |
| `key` | string | Custom field key token. |
| `visibleInPreferenceCenter` | boolean | Whether the field is shown in the subscriber preference center. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /lists/:listId/customfields.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

