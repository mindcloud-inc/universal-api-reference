# SimpleLocalize: List Translations

Retrieves translations from SimpleLocalize.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/list-translations?${params}`, {
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
| `key` | string | no |  |
| `namespace` | string | no |  |
| `language` | string | no |  |
| `text` | string | no |  |
| `query` | string | no |  |
| `textStatus` | list | no | One of: ``, `EMPTY`, `NOT_EMPTY`. |
| `customerId` | string | no |  |
| `baseOnly` | boolean | no |  |
| `reviewStatus` | list | no | One of: ``, `NOT_REVIEWED`, `REVIEWED`. |
| `sortBy` | list | no | One of: ``, `lastModifiedAt`. |
| `sortOrder` | list | no | One of: `asc`, `desc`. |
| `version` | list | no | One of: `REVIEWED`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleLocalize API returns.

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v2/translations` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-translations.md) for the provider-specific parameters and requirements.

