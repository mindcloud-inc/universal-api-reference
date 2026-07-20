# People Data Labs: Autocomplete



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/autocomplete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/autocomplete?connectionId=$CONNECTION_ID&field=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/autocomplete?${params}`, {
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
| `field` | string | yes | Autocomplete field value such as company, title, school, skill, location_name, industry, or website. |
| `text` | string | no | Starting text used as the seed for autocompletion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "meta": {
        "alternativeNames": [
          [
            "Ava Chen"
          ]
        ],
        "displayName": "Ava Chen",
        "displayNameHistory": [
          [
            "Ava Chen"
          ]
        ],
        "id": "string",
        "industry": "string",
        "linkedinSlug": "https://example.com",
        "locationName": "Ava Chen",
        "website": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `meta.alternativeNames[]` | array<string> |  |
| `meta.displayName` | string |  |
| `meta.displayNameHistory[]` | array<string> |  |
| `meta.id` | string |  |
| `meta.industry` | string |  |
| `meta.linkedinSlug` | string |  |
| `meta.locationName` | string |  |
| `meta.website` | string |  |
| `name` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /autocomplete` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete.md) for the provider-specific parameters and requirements.

