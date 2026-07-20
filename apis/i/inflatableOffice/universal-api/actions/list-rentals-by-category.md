# InflatableOffice: List Rentals By Category

Retrieves rentals by category from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-by-category?connectionId=$CONNECTION_ID&limit=25&offset=0&categoryid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "categoryid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-by-category?${params}`, {
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
| `categoryid` | string | yes | ID of the category whose rentals should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": "string",
      "description": "string",
      "Electric": "string",
      "href": "string",
      "id": "string",
      "imageloc": "string",
      "imagelocbig": "string",
      "Is Option": "string",
      "requestTime": 1,
      "ridename": "Ava Chen",
      "Weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | string |  |
| `description` | string |  |
| `Electric` | string |  |
| `href` | string |  |
| `id` | string |  |
| `imageloc` | string |  |
| `imagelocbig` | string |  |
| `Is Option` | string |  |
| `requestTime` | number |  |
| `ridename` | string |  |
| `Weight` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /rentals` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rentals-by-category.md) for the provider-specific parameters and requirements.

