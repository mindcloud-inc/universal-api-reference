# Uploadcare: Get Project

Retrieves current project details from Uploadcare.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-project?${params}`, {
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
      "autostoreEnabled": true,
      "name": "Ava Chen",
      "pubKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autostoreEnabled` | boolean | Whether auto-store is enabled for the project. |
| `name` | string | Uploadcare project name. |
| `pubKey` | string | Project public API key. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /project/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

