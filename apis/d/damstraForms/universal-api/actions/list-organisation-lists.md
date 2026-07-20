# Damstra Forms: List Organisation Lists

Retrieves organisation lists from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-organisation-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-organisation-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-organisation-lists?${params}`, {
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
      "id": 1,
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
| `createdAt` | date | From Damstra Forms API example response. |
| `id` | number | From Damstra Forms API example response. |
| `listLocked` | boolean | From Damstra Forms API example response. |
| `listType` | number | From Damstra Forms API example response. |
| `lockVersion` | number | From Damstra Forms API example response. |
| `name` | string | From Damstra Forms API example response. |
| `titleIndex` | number | From Damstra Forms API example response. |
| `updatedAt` | date | From Damstra Forms API example response. |
| `uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /organisation_lists` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organisation-lists.md) for the provider-specific parameters and requirements.

