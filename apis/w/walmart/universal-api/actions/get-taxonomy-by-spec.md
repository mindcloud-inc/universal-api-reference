# Walmart: Get Taxonomy by Spec

Retrieve a list of all Categories and Sub-categories that are available on Walmart.com for the Item spec version you specify.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy-by-spec
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy-by-spec?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-taxonomy-by-spec?${params}`, {
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
| `feedType` | list<string> | no | The type of feed specifies the nature of the update. Select an option from the drop-down list based on the type of update you need to perform. Example: MP_WFS_ITEM indicates the new WFS Item set up. Example: `item`. |
| `version` | list<list> | no | Specifies the version for the `feedType` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "categoryName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `categoryName` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/utilities/taxonomy` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-taxonomy-by-spec.md) for the provider-specific parameters and requirements.

