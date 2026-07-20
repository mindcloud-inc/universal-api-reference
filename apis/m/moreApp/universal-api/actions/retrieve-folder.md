# MoreApp: Retrieve Folder

Retrieves a folder from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-folder?connectionId=$CONNECTION_ID&customerId=1&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-folder?${params}`, {
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
| `customerId` | number | yes |  |
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        {}
      ],
      "id": "string",
      "meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms` | array<object> |  |
| `id` | string |  |
| `meta` | object |  |
| `status` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-folder.md) for the provider-specific parameters and requirements.

