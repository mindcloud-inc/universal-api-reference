# Pipedrive: Search Deals

Finds deals in Pipedrive by search term.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-deals?connectionId=$CONNECTION_ID&limit=25&offset=0&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-deals?${params}`, {
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
| `cursor` | string | no | Pagination cursor. |
| `fields` | string | no | Fields to search in. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `status` | string | no | Filter by deal status. |
| `term` | string | yes | Search term for deals. |
| `exactMatch` | boolean | no | Match term exactly. |
| `personId` | number | no | Filter by person ID. |
| `organizationId` | number | no | Filter by organization ID. |
| `limit` | number | no | Max results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "item": {
            "currency": "string",
            "id": 1,
            "isArchived": true,
            "organization": {
              "address": {},
              "id": 1,
              "name": "Ava Chen"
            },
            "owner": {
              "id": 1
            },
            "person": {},
            "pipeline": {
              "id": 1
            },
            "stage": {
              "id": 1,
              "name": "Ava Chen"
            },
            "status": "string",
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
| `items[].item.currency` | string |  |
| `items[].item.id` | number |  |
| `items[].item.isArchived` | boolean |  |
| `items[].item.organization.address` | object |  |
| `items[].item.organization.id` | number |  |
| `items[].item.organization.name` | string |  |
| `items[].item.owner.id` | number |  |
| `items[].item.person` | object |  |
| `items[].item.pipeline.id` | number |  |
| `items[].item.stage.id` | number |  |
| `items[].item.stage.name` | string |  |
| `items[].item.status` | string |  |
| `items[].item.title` | string |  |
| `items[].item.type` | string |  |
| `items[].item.value` | object |  |
| `items[].item.visibleTo` | number |  |
| `items[].resultScore` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/deals/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-deals.md) for the provider-specific parameters and requirements.

