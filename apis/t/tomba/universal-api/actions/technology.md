# Tomba: Technology

Retrieves company technology data from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/technology
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/technology?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/technology?${params}`, {
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
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "categories": [
            {
              "name": "Ava Chen"
            }
          ],
          "description": "string",
          "name": "Ava Chen",
          "slug": "string",
          "website": "string"
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
| `[].categories[].name` | string |  |
| `[].description` | string |  |
| `[].name` | string |  |
| `[].slug` | string |  |
| `[].website` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /technology` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/technology.md) for the provider-specific parameters and requirements.

