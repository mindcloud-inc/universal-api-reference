# Youform: List Forms

Lists forms in Youform.

```
GET https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Youform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-forms?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultLanguage": "string",
      "design": {},
      "draftFields": {},
      "emailNotification": {},
      "fields": {},
      "id": 1,
      "name": "Ava Chen",
      "poweredByHidden": 1,
      "slug": "string",
      "submissionsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `defaultLanguage` | string |  |
| `design` | object |  |
| `draftFields` | object |  |
| `emailNotification` | object |  |
| `fields` | object |  |
| `id` | number |  |
| `name` | string |  |
| `poweredByHidden` | number |  |
| `slug` | string |  |
| `submissionsCount` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Youform API, this operation is `GET /forms` (base URL `https://app.youform.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

