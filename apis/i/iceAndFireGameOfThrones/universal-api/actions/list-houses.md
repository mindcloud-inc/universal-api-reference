# Ice and Fire (Game of Thrones): List Houses



```
GET https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-houses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ice and Fire (Game of Thrones) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-houses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-houses?${params}`, {
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
| `name` | string | no | Return only houses with this exact name. |
| `region` | string | no | Return only houses from this region. |
| `words` | string | no | Return only houses with these words. |
| `hasWords` | boolean | no | Return only houses that do or do not have words. |
| `hasTitles` | boolean | no | Return only houses that do or do not have titles. |
| `hasSeats` | boolean | no | Return only houses that do or do not have seats. |
| `hasDiedOut` | boolean | no | Return only houses that have or have not died out. |
| `hasAncestralWeapons` | boolean | no | Return only houses that do or do not have ancestral weapons. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ancestralWeapons": [
        "string"
      ],
      "cadetBranches": [
        "string"
      ],
      "coatOfArms": "string",
      "currentLord": "string",
      "diedOut": "string",
      "founded": "string",
      "founder": "string",
      "heir": "string",
      "name": "Ava Chen",
      "overlord": "string",
      "region": "string",
      "seats": [
        "string"
      ],
      "swornMembers": [
        "string"
      ],
      "titles": [
        "string"
      ],
      "url": "https://example.com",
      "words": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ancestralWeapons` | array<string> |  |
| `cadetBranches` | array<string> |  |
| `coatOfArms` | string |  |
| `currentLord` | string |  |
| `diedOut` | string |  |
| `founded` | string |  |
| `founder` | string |  |
| `heir` | string |  |
| `name` | string |  |
| `overlord` | string |  |
| `region` | string |  |
| `seats` | array<string> |  |
| `swornMembers` | array<string> |  |
| `titles` | array<string> |  |
| `url` | string |  |
| `words` | string |  |

## Native endpoint

Through the native Ice and Fire (Game of Thrones) API, this operation is `GET /houses` (base URL `https://anapioficeandfire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-houses.md) for the provider-specific parameters and requirements.

