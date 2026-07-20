# Global Patron: List Datalist Entry Items

Lists datalist entry items in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-datalist-entry-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-datalist-entry-items?connectionId=$CONNECTION_ID&datalistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datalistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-datalist-entry-items?${params}`, {
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
| `datalistId` | string | yes | ID of the datalist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "createdDateUtc": "2026-05-07T12:00:00.000Z",
          "datalistId": "string",
          "entryItemValues": [
            {
              "label": "string",
              "value": "string"
            }
          ],
          "id": "string",
          "modifiedDateUtc": "2026-05-07T12:00:00.000Z"
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
| `results` | array<object> | Datalist entry items. |
| `results[].createdDateUtc` | date | Creation timestamp. |
| `results[].datalistId` | string | Datalist identifier. |
| `results[].entryItemValues` | array<object> | Entry item values. |
| `results[].entryItemValues[].label` | string | Entry item label. |
| `results[].entryItemValues[].value` | string | Entry item value. |
| `results[].id` | string | Datalist entry identifier. |
| `results[].modifiedDateUtc` | date | Last modification timestamp. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/datalist/{datalistId}/entries` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datalist-entry-items.md) for the provider-specific parameters and requirements.

