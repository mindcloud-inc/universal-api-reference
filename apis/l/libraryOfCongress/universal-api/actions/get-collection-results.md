# Library of Congress: Get Collection Results

Retrieves results from a Library of Congress collection.

```
GET https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Library of Congress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection-results?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collectionSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection-results?${params}`, {
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
| `collectionSlug` | string | yes | The kebab-case loc.gov collection slug, such as civil-war-maps or baseball-cards. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Library of Congress API returns.

## Native endpoint

Through the native Library of Congress API, this operation is `GET /collections/{collectionSlug}/` (base URL `https://www.loc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-collection-results.md) for the provider-specific parameters and requirements.

