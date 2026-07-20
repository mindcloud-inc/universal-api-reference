# Brevo: List Lists in Folder



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists-in-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists-in-folder?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-lists-in-folder?${params}`, {
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
| `folderId` | number | yes | The contact folder identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "lists": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | The number of lists. |
| `lists` | array<object> | The lists in the folder. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/folders/:folderId/lists` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists-in-folder.md) for the provider-specific parameters and requirements.

