# Constant Contact: Delete Contact List

Deletes a contact list from Constant Contact.

```
DELETE https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-list?connectionId=$CONNECTION_ID&listId=4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/delete-contact-list?${params}`, {
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
| `listId` | string | yes | Unique ID of the list to delete. Example: `4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityErrors": [
        "string"
      ],
      "activityId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "links": {},
      "percentDone": 1,
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityErrors` | array<string> |  |
| `activityId` | string |  |
| `createdAt` | date |  |
| `links` | object |  |
| `percentDone` | number |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `DELETE /contact_lists/:list_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-list.md) for the provider-specific parameters and requirements.

