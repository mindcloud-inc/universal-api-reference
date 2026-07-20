# Constant Contact: Delete Contact Tag

Deletes a contact tag from Constant Contact.

```
DELETE https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-tag?connectionId=$CONNECTION_ID&tagId=cc4f2295-76bd-44f3-a07f-1ea4be3f1473" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "cc4f2295-76bd-44f3-a07f-1ea4be3f1473"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-tag?${params}`, {
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
| `tagId` | string | yes | UUID of the tag to delete. Example: `cc4f2295-76bd-44f3-a07f-1ea4be3f1473`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityErrors": [
        {}
      ],
      "activityId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "links": {},
      "percentDone": 1,
      "state": "string",
      "status": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityErrors` | array<object> |  |
| `activityId` | string |  |
| `createdAt` | date |  |
| `links` | object |  |
| `percentDone` | number |  |
| `state` | string |  |
| `status` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `DELETE /contact_tags/:tag_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-tag.md) for the provider-specific parameters and requirements.

