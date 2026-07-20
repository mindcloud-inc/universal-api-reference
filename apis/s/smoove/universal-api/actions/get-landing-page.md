# Smoove: Get Landing Page

Retrieves a landing page from Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-landing-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-landing-page?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/get-landing-page?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": 1,
      "formTitle": "string",
      "formType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | number |  |
| `formTitle` | string |  |
| `formType` | string |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/LandingPages/:id` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-landing-page.md) for the provider-specific parameters and requirements.

