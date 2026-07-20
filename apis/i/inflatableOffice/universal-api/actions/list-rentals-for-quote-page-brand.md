# InflatableOffice: List Rentals For Quote Page / Brand

Retrieves rentals for a quote page brand from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-for-quote-page-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-for-quote-page-brand?connectionId=$CONNECTION_ID&limit=25&offset=0&pageName=Demo%20Rentals%20LLC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pageName": "Demo Rentals LLC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-rentals-for-quote-page-brand?${params}`, {
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
| `pageName` | string | yes | Quote page or brand group name from the page templates. Example: `Demo Rentals LLC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": "string",
      "description": "string",
      "href": "string",
      "id": "string",
      "imageloc": "string",
      "imagelocbig": "string",
      "Is Option": "string",
      "Packing List": "string",
      "ridename": "Ava Chen"
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
| `href` | string |  |
| `id` | string |  |
| `imageloc` | string |  |
| `imagelocbig` | string |  |
| `Is Option` | string |  |
| `Packing List` | string |  |
| `ridename` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /rentals` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rentals-for-quote-page-brand.md) for the provider-specific parameters and requirements.

