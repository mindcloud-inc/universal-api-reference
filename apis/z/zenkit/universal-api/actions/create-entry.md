# Zenkit: Create Entry

Creates a new item in Zenkit.

```
POST https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/create-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The list id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "156070e1-0820-4d98-945f-d1b89cb195be_searchText": "string",
      "156070e1-0820-4d98-945f-d1b89cb195be_text": "string",
      "156070e1-0820-4d98-945f-d1b89cb195be_textType": "string",
      "2ac63081-bac2-4b94-8b57-3ffecf576128_searchText": "string",
      "2ac63081-bac2-4b94-8b57-3ffecf576128_text": "string",
      "2ac63081-bac2-4b94-8b57-3ffecf576128_textType": "string",
      "402328e1-1f8b-4b0c-9f5e-66141d72d54a_connected": true,
      "402328e1-1f8b-4b0c-9f5e-66141d72d54a_path": "string",
      "402328e1-1f8b-4b0c-9f5e-66141d72d54a_sortOrder": 1,
      "58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort": [
        {
          "colorHex": "string",
          "id": 1,
          "name": "Ava Chen",
          "uuid": "string"
        }
      ],
      "58e9414d-661e-4c9f-bed2-ef32f7111d17_categories": [
        1
      ],
      "81b6f6e1-2199-44ee-a6dd-312a10523f3d_milestone": true,
      "9afd86b1-c1f6-4270-ac2b-4ae061a314d9_date": "string",
      "9afd86b1-c1f6-4270-ac2b-4ae061a314d9_duration": "string",
      "9afd86b1-c1f6-4270-ac2b-4ae061a314d9_endDate": "string",
      "9afd86b1-c1f6-4270-ac2b-4ae061a314d9_hasTime": true,
      "cf945125-e721-42d5-93f1-a2259248a41a_number": "string",
      "comment_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "created_by_displayname": "Ava Chen",
      "deprecated_at": "string",
      "deprecated_by": "string",
      "displayString": "string",
      "id": 1,
      "listId": 1,
      "occurrence": "string",
      "origin_created_at": "string",
      "shortId": "string",
      "sortOrder": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_by": 1,
      "updated_by_displayname": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `156070e1-0820-4d98-945f-d1b89cb195be_searchText` | string |  |
| `156070e1-0820-4d98-945f-d1b89cb195be_text` | string |  |
| `156070e1-0820-4d98-945f-d1b89cb195be_textType` | string |  |
| `2ac63081-bac2-4b94-8b57-3ffecf576128_searchText` | string |  |
| `2ac63081-bac2-4b94-8b57-3ffecf576128_text` | string |  |
| `2ac63081-bac2-4b94-8b57-3ffecf576128_textType` | string |  |
| `402328e1-1f8b-4b0c-9f5e-66141d72d54a_connected` | boolean |  |
| `402328e1-1f8b-4b0c-9f5e-66141d72d54a_path` | string |  |
| `402328e1-1f8b-4b0c-9f5e-66141d72d54a_sortOrder` | number |  |
| `58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].colorHex` | string |  |
| `58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].id` | number |  |
| `58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].name` | string |  |
| `58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].uuid` | string |  |
| `58e9414d-661e-4c9f-bed2-ef32f7111d17_categories[]` | number |  |
| `81b6f6e1-2199-44ee-a6dd-312a10523f3d_milestone` | boolean |  |
| `9afd86b1-c1f6-4270-ac2b-4ae061a314d9_date` | string |  |
| `9afd86b1-c1f6-4270-ac2b-4ae061a314d9_duration` | string |  |
| `9afd86b1-c1f6-4270-ac2b-4ae061a314d9_endDate` | string |  |
| `9afd86b1-c1f6-4270-ac2b-4ae061a314d9_hasTime` | boolean |  |
| `cf945125-e721-42d5-93f1-a2259248a41a_number` | string |  |
| `comment_count` | number |  |
| `created_at` | date |  |
| `created_by` | number |  |
| `created_by_displayname` | string |  |
| `deprecated_at` | string |  |
| `deprecated_by` | string |  |
| `displayString` | string |  |
| `id` | number |  |
| `listId` | number |  |
| `occurrence` | string |  |
| `origin_created_at` | string |  |
| `shortId` | string |  |
| `sortOrder` | string |  |
| `updated_at` | date |  |
| `updated_by` | number |  |
| `updated_by_displayname` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `POST /lists/:listId/entries` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entry.md) for the provider-specific parameters and requirements.

