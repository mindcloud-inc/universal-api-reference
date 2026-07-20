# Paperform: List Form Coupons

Retrieves coupons from a Paperform form.

```
GET https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-coupons?connectionId=$CONNECTION_ID&slugOrId=contact-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slugOrId": "contact-form"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-form-coupons?${params}`, {
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
| `slugOrId` | list<string> | yes | Example: `contact-form`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discountAmount": 1,
      "discountPercentage": 1,
      "enabled": true,
      "formSlugOrId": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discountAmount` | number |  |
| `discountPercentage` | number |  |
| `enabled` | boolean |  |
| `formSlugOrId` | string | Form slug or ID used to build the Paperform editor URL. |
| `target` | string |  |

## Native endpoint

Through the native Paperform API, this operation is `GET /forms/:slug_or_id/coupons` (base URL `https://api.paperform.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-coupons.md) for the provider-specific parameters and requirements.

