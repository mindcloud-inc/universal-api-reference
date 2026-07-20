# OfficeClip: List Notes

Retrieves notes from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-notes?${params}`, {
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
      "createdByTimestampFieldSpecified": true,
      "createdByUserNameField": "Ava Chen",
      "createdByUserSidField": "string",
      "descriptionField": "string",
      "isLockFieldSpecified": true,
      "isPrivateFieldSpecified": true,
      "modifiedByTimestampFieldSpecified": true,
      "modifiedByUserNameField": {},
      "modifiedByUserSidField": "string",
      "noteBookNameField": "Ava Chen",
      "noteBookSidField": "string",
      "noteIdFieldSpecified": true,
      "parentObjectServiceTypeFieldSpecified": true,
      "parentObjectSidField": "string",
      "regardingField": "string",
      "sidField": "string",
      "subjectField": "string",
      "tagField": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByTimestampFieldSpecified` | boolean |  |
| `createdByUserNameField` | string |  |
| `createdByUserSidField` | string |  |
| `descriptionField` | string |  |
| `isLockFieldSpecified` | boolean |  |
| `isPrivateFieldSpecified` | boolean |  |
| `modifiedByTimestampFieldSpecified` | boolean |  |
| `modifiedByUserNameField` | object |  |
| `modifiedByUserSidField` | string |  |
| `noteBookNameField` | string |  |
| `noteBookSidField` | string |  |
| `noteIdFieldSpecified` | boolean |  |
| `parentObjectServiceTypeFieldSpecified` | boolean |  |
| `parentObjectSidField` | string |  |
| `regardingField` | string |  |
| `sidField` | string |  |
| `subjectField` | string |  |
| `tagField` | string |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/note` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

