# Tidio: Get Viewed Pages History [Plus plan]

Retrieves viewed page history for a contact in Tidio.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-viewed-pages-history-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-viewed-pages-history-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-viewed-pages-history-plus-plan?${params}`, {
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
| `contactId` | string | yes | The Tidio contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "cursor": "string",
        "limit": 1
      },
      "viewedPages": [
        {
          "url": "https://example.com",
          "viewedAt": "2026-05-07T12:00:00.000Z"
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
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |
| `viewedPages` | array<object> |  |
| `viewedPages[]` | object |  |
| `viewedPages[].url` | string | URL of viewed page |
| `viewedPages[].viewedAt` | date | Date when page has been viewed |

## Native endpoint

Through the native Tidio API, this operation is `GET /contacts/{contactId}/viewed-pages` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-viewed-pages-history-plus-plan.md) for the provider-specific parameters and requirements.

