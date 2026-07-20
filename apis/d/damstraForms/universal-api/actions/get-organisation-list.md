# Damstra Forms: Get Organisation List

Retrieves an organisation list from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-organisation-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-organisation-list?connectionId=$CONNECTION_ID&id=1%20or%20848ab438-9bae-4237-acd8-900dd04b385c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1 or 848ab438-9bae-4237-acd8-900dd04b385c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-organisation-list?${params}`, {
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
| `id` | string | yes | The unique id (numeric) or uuid (string) of the organisation list. Example: `1 or 848ab438-9bae-4237-acd8-900dd04b385c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnHeadings": [
        "string"
      ],
      "columnTypes": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "itemTable": [
        [
          "string"
        ]
      ],
      "listLocked": true,
      "listType": 1,
      "lockVersion": 1,
      "name": "Ava Chen",
      "titleIndex": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnHeadings` | array<string> | From Damstra Forms API example response. |
| `columnTypes` | array<string> | From Damstra Forms API example response. |
| `createdAt` | date | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `itemTable` | array<array> | From Damstra Forms API example response. |
| `listLocked` | boolean | From Damstra Forms API example response. |
| `listType` | number | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `titleIndex` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /organisation_lists/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation-list.md) for the provider-specific parameters and requirements.

