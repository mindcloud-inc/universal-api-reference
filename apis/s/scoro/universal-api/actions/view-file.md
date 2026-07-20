# Scoro: View File

Retrieves file details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-file?${params}`, {
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
| `id` | string | no | Scoro file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_id": 1,
      "modified_date": "string",
      "name": "Ava Chen",
      "size": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_id` | number |  |
| `modified_date` | string |  |
| `name` | string |  |
| `size` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST files/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-file.md) for the provider-specific parameters and requirements.

