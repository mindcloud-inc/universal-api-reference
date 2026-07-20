# People Data Labs: Clean School



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-school
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-school?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-school?${params}`, {
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
| `name` | string | yes | School name to standardize into canonical school data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "facebookUrl": "https://example.com",
      "id": "string",
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "location": {
        "continent": "string",
        "country": "string",
        "locality": "string",
        "name": "Ava Chen",
        "region": "string"
      },
      "matchedOn": [
        [
          "string"
        ]
      ],
      "name": "Ava Chen",
      "status": 1,
      "twitterUrl": "https://example.com",
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `facebookUrl` | string |  |
| `id` | string |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `location.continent` | string |  |
| `location.country` | string |  |
| `location.locality` | string |  |
| `location.name` | string |  |
| `location.region` | string |  |
| `matchedOn[]` | array<string> |  |
| `name` | string |  |
| `status` | number |  |
| `twitterUrl` | string |  |
| `type` | string |  |
| `website` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /school/clean` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clean-school.md) for the provider-specific parameters and requirements.

