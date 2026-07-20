# Zenkit: Get Filtered Entries For List View

Retrieves filtered items for a Zenkit list view.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-filtered-entries-for-list-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-filtered-entries-for-list-view?connectionId=$CONNECTION_ID&listShortId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listShortId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-filtered-entries-for-list-view?${params}`, {
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
| `listShortId` | string | yes | The list short id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countData": {
        "filteredTotal": 1,
        "total": 1
      },
      "countDataPerGroup": [
        {
          "58e9414d-661e-4c9f-bed2-ef32f7111d17_categories": [
            1
          ],
          "filteredTotal": 1,
          "total": 1
        }
      ],
      "listEntries": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countData.filteredTotal` | number |  |
| `countData.total` | number |  |
| `countDataPerGroup[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories[]` | number |  |
| `countDataPerGroup[].filteredTotal` | number |  |
| `countDataPerGroup[].total` | number |  |
| `listEntries[].156070e1-0820-4d98-945f-d1b89cb195be_searchText` | string |  |
| `listEntries[].156070e1-0820-4d98-945f-d1b89cb195be_text` | string |  |
| `listEntries[].156070e1-0820-4d98-945f-d1b89cb195be_textType` | string |  |
| `listEntries[].2ac63081-bac2-4b94-8b57-3ffecf576128_searchText` | string |  |
| `listEntries[].2ac63081-bac2-4b94-8b57-3ffecf576128_text` | string |  |
| `listEntries[].2ac63081-bac2-4b94-8b57-3ffecf576128_textType` | string |  |
| `listEntries[].402328e1-1f8b-4b0c-9f5e-66141d72d54a_connected` | boolean |  |
| `listEntries[].402328e1-1f8b-4b0c-9f5e-66141d72d54a_path` | string |  |
| `listEntries[].402328e1-1f8b-4b0c-9f5e-66141d72d54a_sortOrder` | number |  |
| `listEntries[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].colorHex` | string |  |
| `listEntries[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].id` | number |  |
| `listEntries[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].name` | string |  |
| `listEntries[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories_sort[].uuid` | string |  |
| `listEntries[].58e9414d-661e-4c9f-bed2-ef32f7111d17_categories[]` | number |  |
| `listEntries[].81b6f6e1-2199-44ee-a6dd-312a10523f3d_milestone` | boolean |  |
| `listEntries[].9afd86b1-c1f6-4270-ac2b-4ae061a314d9_date` | string |  |
| `listEntries[].9afd86b1-c1f6-4270-ac2b-4ae061a314d9_duration` | string |  |
| `listEntries[].9afd86b1-c1f6-4270-ac2b-4ae061a314d9_endDate` | string |  |
| `listEntries[].9afd86b1-c1f6-4270-ac2b-4ae061a314d9_hasTime` | boolean |  |
| `listEntries[].cf945125-e721-42d5-93f1-a2259248a41a_number` | string |  |
| `listEntries[].comment_count` | number |  |
| `listEntries[].created_at` | date |  |
| `listEntries[].created_by` | number |  |
| `listEntries[].created_by_displayname` | string |  |
| `listEntries[].deprecated_at` | string |  |
| `listEntries[].deprecated_by` | string |  |
| `listEntries[].displayString` | string |  |
| `listEntries[].id` | number |  |
| `listEntries[].listId` | number |  |
| `listEntries[].occurrence` | string |  |
| `listEntries[].origin_created_at` | string |  |
| `listEntries[].shortId` | string |  |
| `listEntries[].sortOrder` | string |  |
| `listEntries[].updated_at` | date |  |
| `listEntries[].updated_by` | number |  |
| `listEntries[].updated_by_displayname` | string |  |
| `listEntries[].uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `POST /lists/:listShortId/entries/filter/list` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filtered-entries-for-list-view.md) for the provider-specific parameters and requirements.

