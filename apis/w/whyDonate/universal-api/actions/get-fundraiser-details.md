# WhyDonate: Get Fundraiser Details



```
GET https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-fundraiser-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhyDonate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-fundraiser-details?connectionId=$CONNECTION_ID&slug=save-the-children" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "save-the-children"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whyDonate/latest/actions/get-fundraiser-details?${params}`, {
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
| `slug` | string | yes | Fundraiser slug used by WhyDonate public pages and widgets. Example: `save-the-children`. |
| `language` | string | no | Language code passed by the WhyDonate widget when fetching fundraiser details. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountTarget": 1,
      "category": {
        "name": "Ava Chen"
      },
      "currencyCode": "string",
      "currencySymbol": "string",
      "donation": {
        "amount": 1,
        "count": 1
      },
      "id": 1,
      "isDraft": true,
      "isOpened": true,
      "languageCode": "string",
      "location": {
        "locationName": "Ava Chen"
      },
      "profile": {
        "image": "string",
        "name": "Ava Chen"
      },
      "slug": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountTarget` | number |  |
| `category.name` | string |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `donation.amount` | number |  |
| `donation.count` | number |  |
| `id` | number |  |
| `isDraft` | boolean |  |
| `isOpened` | boolean |  |
| `languageCode` | string |  |
| `location.locationName` | string |  |
| `profile.image` | string |  |
| `profile.name` | string |  |
| `slug` | string |  |
| `title` | string |  |

## Native endpoint

Through the native WhyDonate API, this operation is `GET /fundraiser/get` (base URL `https://fundraiser.whydonate.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fundraiser-details.md) for the provider-specific parameters and requirements.

