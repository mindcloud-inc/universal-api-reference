# Document360: List Project Versions



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions?${params}`, {
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
      "baseVersionNumber": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isBeta": true,
      "isDeprecated": true,
      "isMainVersion": true,
      "isPublic": true,
      "languageVersions": [
        {}
      ],
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "order": 1,
      "slug": "string",
      "versionCodeName": "Ava Chen",
      "versionNumber": 1,
      "versionType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseVersionNumber` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isBeta` | boolean |  |
| `isDeprecated` | boolean |  |
| `isMainVersion` | boolean |  |
| `isPublic` | boolean |  |
| `languageVersions` | array<object> |  |
| `modifiedAt` | date |  |
| `order` | number |  |
| `slug` | string |  |
| `versionCodeName` | string |  |
| `versionNumber` | number |  |
| `versionType` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/ProjectVersions` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-versions.md) for the provider-specific parameters and requirements.

