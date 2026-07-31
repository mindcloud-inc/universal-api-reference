# Ice and Fire (Game of Thrones): Get House



```
GET https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-house
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ice and Fire (Game of Thrones) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-house?connectionId=$CONNECTION_ID&houseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "houseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-house?${params}`, {
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
| `houseId` | number | yes | The numeric ID of the house to retrieve. |

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

Through the native Ice and Fire (Game of Thrones) API, this operation is `GET /houses/:houseId` (base URL `https://anapioficeandfire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-house.md) for the provider-specific parameters and requirements.

