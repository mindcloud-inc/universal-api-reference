# Random User: Generate Random Users



```
GET https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Random User `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users?${params}`, {
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
| `results` | number | no | Number of users to generate (1 to 5000). Default: `1`. Example: `1–5000`. |
| `nationalities` | list | no | Optional nationalities to include. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `20`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Accepts multiple values in one string, delimited by `,`. |
| `gender` | list | no | Optional generated user gender. One of: `0`, `1`. |
| `seed` | string | no | Optional deterministic seed for reproducible results. Example: `e.g., test-seed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `password_options` | string | no | Password grammar: charsets,MIN_LENGTH-MAX_LENGTH or charsets,MAX_LENGTH. Example: `e.g., upper,lower,8-16`. |
| `include_fields` | list | no | Optional comma-delimited fields to include. One of: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Accepts multiple values in one string, delimited by `,`. |
| `exclude_fields` | list | no | Optional comma-delimited fields to exclude. One of: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {
        "page": 1,
        "results": 1,
        "seed": "string",
        "version": "string"
      },
      "results": [
        {
          "cell": "string",
          "dob": {
            "age": 1,
            "date": "2026-05-07T12:00:00.000Z"
          },
          "email": "ava@example.com",
          "gender": "string",
          "id": {
            "name": "Ava Chen",
            "value": "string"
          },
          "location": {
            "city": "string",
            "coordinates": {
              "latitude": "string",
              "longitude": "string"
            },
            "country": "string",
            "state": "string",
            "street": {
              "name": "Ava Chen",
              "number": 1
            },
            "timezone": {
              "description": "string",
              "offset": "string"
            }
          },
          "login": {
            "password": "string",
            "username": "Ava Chen",
            "uuid": "string"
          },
          "name": {
            "first": "Ava Chen",
            "last": "Ava Chen",
            "title": "Ava Chen"
          },
          "nat": "string",
          "phone": "string",
          "picture": {
            "large": "string",
            "medium": "string",
            "thumbnail": "string"
          },
          "registered": {
            "age": 1,
            "date": "2026-05-07T12:00:00.000Z"
          }
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
| `info` | object | Generation metadata. |
| `info.page` | number |  |
| `info.results` | number |  |
| `info.seed` | string |  |
| `info.version` | string |  |
| `results` | array<object> | Generated synthetic user profiles. |
| `results[].cell` | string |  |
| `results[].dob` | object |  |
| `results[].dob.age` | number |  |
| `results[].dob.date` | date |  |
| `results[].email` | string |  |
| `results[].gender` | string |  |
| `results[].id` | object |  |
| `results[].id.name` | string |  |
| `results[].id.value` | string |  |
| `results[].location` | object |  |
| `results[].location.city` | string |  |
| `results[].location.coordinates` | object |  |
| `results[].location.coordinates.latitude` | string |  |
| `results[].location.coordinates.longitude` | string |  |
| `results[].location.country` | string |  |
| `results[].location.state` | string |  |
| `results[].location.street` | object |  |
| `results[].location.street.name` | string |  |
| `results[].location.street.number` | number |  |
| `results[].location.timezone` | object |  |
| `results[].location.timezone.description` | string |  |
| `results[].location.timezone.offset` | string |  |
| `results[].login` | object |  |
| `results[].login.password` | string |  |
| `results[].login.username` | string |  |
| `results[].login.uuid` | string |  |
| `results[].name` | object |  |
| `results[].name.first` | string |  |
| `results[].name.last` | string |  |
| `results[].name.title` | string |  |
| `results[].nat` | string |  |
| `results[].phone` | string |  |
| `results[].picture` | object |  |
| `results[].picture.large` | string |  |
| `results[].picture.medium` | string |  |
| `results[].picture.thumbnail` | string |  |
| `results[].registered` | object |  |
| `results[].registered.age` | number |  |
| `results[].registered.date` | date |  |

## Native endpoint

Through the native Random User API, this operation is `GET /api/` (base URL `https://randomuser.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-random-users.md) for the provider-specific parameters and requirements.

