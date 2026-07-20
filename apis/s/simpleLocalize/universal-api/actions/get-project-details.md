# SimpleLocalize: Get Project Details

Retrieves project details from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details?${params}`, {
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
      "createdAt": "string",
      "customers": [
        {}
      ],
      "environments": [
        {}
      ],
      "hostingResources": [
        {}
      ],
      "keys": 1,
      "languages": [
        {}
      ],
      "lastActivityAt": "string",
      "lastEditedAt": "string",
      "name": "Ava Chen",
      "namespaces": [
        {}
      ],
      "projectToken": "string",
      "translatedKeysByLanguage": {},
      "translatedPercentage": 1,
      "unpublishedChanges": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `customers` | array<object> |  |
| `environments` | array<object> |  |
| `hostingResources` | array<object> |  |
| `keys` | number |  |
| `languages` | array<object> |  |
| `lastActivityAt` | string |  |
| `lastEditedAt` | string |  |
| `name` | string |  |
| `namespaces` | array<object> |  |
| `projectToken` | string |  |
| `translatedKeysByLanguage` | object |  |
| `translatedPercentage` | number |  |
| `unpublishedChanges` | number |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v2/project` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-details.md) for the provider-specific parameters and requirements.

