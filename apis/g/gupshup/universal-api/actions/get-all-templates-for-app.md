# Gupshup: Get All Templates For App

Retrieves all templates for a Gupshup app.

```
GET https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-all-templates-for-app?${params}`, {
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
| `appId` | string | yes | Gupshup app ID. |
| `languageCode` | string | no | Filter templates by language code. |
| `quality` | string | no | Filter templates by quality rating. |
| `templateCategory` | string | no | Filter templates by category: marketing, utility, or authentication. |
| `templateStatus` | string | no | Filter templates by status, for example APPROVED. |
| `templateType` | string | no | Filter templates by template type. |
| `pageNo` | number | no | Page number for paginated template results. |
| `pageSize` | number | no | Number of templates per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNo": 1,
      "pageSize": 1,
      "templates": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNo` | number | Returned page number when provided by Gupshup. |
| `pageSize` | number | Returned page size when provided by Gupshup. |
| `templates` | array<object> | Templates returned for the app. |
| `total` | number | Total template count when provided by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `GET /wa/app/{app_id}/template` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-templates-for-app.md) for the provider-specific parameters and requirements.

