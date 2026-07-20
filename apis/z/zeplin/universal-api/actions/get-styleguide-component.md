# Zeplin: Get Styleguide Component

Retrieves a styleguide component from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component?connectionId=$CONNECTION_ID&styleguideId=string&componentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleguideId": "string",
  "componentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-component?${params}`, {
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
| `styleguideId` | string | yes | Styleguide id |
| `componentId` | string | yes | Component id |
| `linkedProject` | string | no | Reference project id |
| `linkedStyleguide` | string | no | Reference styleguide id |
| `includeLatestVersion` | boolean | no | Whether to include the latest version data in the Component object |
| `includeLinkedStyleguides` | boolean | no | Whether to include linked styleguides or not |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "description": "string",
      "id": "string",
      "image": {},
      "name": "Ava Chen",
      "section": {},
      "source": {},
      "updated": 1,
      "variant_properties": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `description` | string |  |
| `id` | string |  |
| `image` | object |  |
| `name` | string |  |
| `section` | object |  |
| `source` | object |  |
| `updated` | number |  |
| `variant_properties` | array<object> |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/components/{component_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-styleguide-component.md) for the provider-specific parameters and requirements.

