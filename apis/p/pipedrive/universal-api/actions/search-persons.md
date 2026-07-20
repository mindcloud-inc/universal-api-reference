# Pipedrive: Search Persons

Finds people in Pipedrive by search term.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-persons?connectionId=$CONNECTION_ID&limit=25&offset=0&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-persons?${params}`, {
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
| `term` | string | yes | Search term for persons. |
| `fields` | string | no | Comma-separated fields to search in. |
| `exactMatch` | boolean | no | Set true to return only exact matches. |
| `organizationId` | number | no | Limit search to a specific organization ID. |
| `personId` | number | no | Limit search to a specific person ID. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `customFields` | string | no | Comma-separated custom field keys to include. |
| `limit` | number | no | Maximum number of search results to return. |
| `cursor` | string | no | Pagination cursor from previous search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "item": {
            "id": 1,
            "name": "Ava Chen",
            "organization": {
              "address": {},
              "id": 1,
              "name": "Ava Chen"
            },
            "owner": {
              "id": 1
            },
            "primaryEmail": {},
            "type": "string",
            "updateTime": "string",
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
| `items[].item.id` | number |  |
| `items[].item.name` | string |  |
| `items[].item.organization.address` | object |  |
| `items[].item.organization.id` | number |  |
| `items[].item.organization.name` | string |  |
| `items[].item.owner.id` | number |  |
| `items[].item.primaryEmail` | object |  |
| `items[].item.type` | string |  |
| `items[].item.updateTime` | string |  |
| `items[].item.visibleTo` | number |  |
| `items[].resultScore` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/persons/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-persons.md) for the provider-specific parameters and requirements.

