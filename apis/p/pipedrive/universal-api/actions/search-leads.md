# Pipedrive: Search Leads

Finds leads in Pipedrive by search term.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-leads?${params}`, {
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
| `term` | string | yes | Search term for lead name/title/email. |
| `exactMatch` | boolean | no | Set true to only return exact matches. |
| `limit` | number | no | Max number of results to return. |
| `cursor` | string | no | Pagination cursor from previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "item": {
            "currency": {},
            "id": "string",
            "isArchived": true,
            "organization": {
              "id": 1,
              "name": "Ava Chen"
            },
            "owner": {
              "id": 1
            },
            "person": {},
            "title": "string",
            "type": "string",
            "value": {},
            "visibleTo": 1
          },
          "resultScore": 1
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
| `items[].item.currency` | object |  |
| `items[].item.id` | string |  |
| `items[].item.isArchived` | boolean |  |
| `items[].item.organization.id` | number |  |
| `items[].item.organization.name` | string |  |
| `items[].item.owner.id` | number |  |
| `items[].item.person` | object |  |
| `items[].item.title` | string |  |
| `items[].item.type` | string |  |
| `items[].item.value` | object |  |
| `items[].item.visibleTo` | number |  |
| `items[].resultScore` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/leads/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-leads.md) for the provider-specific parameters and requirements.

