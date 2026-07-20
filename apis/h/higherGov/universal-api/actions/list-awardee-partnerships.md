# HigherGov: List Awardee Partnerships

Retrieves awardee partnerships from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardee-partnerships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardee-partnerships?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-awardee-partnerships?${params}`, {
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
| `awardeeKeyPrime` | string | no | HigherGov Awardee Key of the prime recipient |
| `awardeeKeyPrimeParent` | string | no | HigherGov Awardee Key of the prime recipient parent |
| `awardeeKeySub` | string | no | HigherGov Awardee Key of the subawardee |
| `awardeeKeySubParent` | string | no | HigherGov Awardee Key of the subawardee parent |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awardee_key_prime": {},
      "awardee_key_sub": {},
      "most_recent_date": "string",
      "number_of_awards": 1,
      "relationship_type": "string",
      "total_awards": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awardee_key_prime` | object |  |
| `awardee_key_sub` | object |  |
| `most_recent_date` | string |  |
| `number_of_awards` | number |  |
| `relationship_type` | string |  |
| `total_awards` | number |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/awardee-partnership/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-awardee-partnerships.md) for the provider-specific parameters and requirements.

