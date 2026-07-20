# Selzy: Export Contacts

Exports contacts from Selzy.

```
GET https://connect.mindcloud.co/v1/universal/selzy/latest/actions/export-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/export-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/export-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "file_to_download": "string",
        "status": "string",
        "task_type": "string",
        "task_uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.file_to_download` | string |  |
| `result.status` | string |  |
| `result.task_type` | string |  |
| `result.task_uuid` | string |  |

## Native endpoint

Through the native Selzy API, this operation is `POST exportContacts` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-contacts.md) for the provider-specific parameters and requirements.

